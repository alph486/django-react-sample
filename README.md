# django-react-sample
A project using django-rest-framework to power a react app. Based on https://www.valentinog.com/blog/tutorial-api-django-rest-react/


# On State Management: Note to self
The list doesn't update state automatically when a new entry is submitted, which is not good. In looking into ways to do this, the seemingly straightforward way, given that `Form` and `Table` are independent compoenents, is to use a state management system to share the state input by the form to the table. I'm getting the vibe that state management like Redux or React Context should be used _only if_ passing properties and composition of components does not work.

To refactor this to do that, I guess you could compose them into one page component and have both of their state passed into them and shared between them; so basically they'd be one component representing this "page". It wouldnt make sense for one to be a child of the other.

Another thought is that this style of form and list view isn't a good design for a single page app... you would probably have the form more neatly integrated into the list view so that they could, in fact, be one component and share their state.

This is an interesting exercise in terms of how React makes you think about app design.
