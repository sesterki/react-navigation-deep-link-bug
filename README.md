# react-navigation-deep-link-bug

The bug I encountered is that a deep link which opens the app (the app was killed/closed/etc, not backgrounded), opens both the Initial Route and the route specified by the deep link.

This project reproduces an issue with react navigation.
Steps:
1. Clone the repo
2. Run the project with expo
3. Make note of the deep link prefix printed to the console
4. Test [prefix]/Main/one and [prefix]/Main/two and note that the render functions print when they are supposed to
5. Close/kill the app (swipe it out of backgrounded tasks etc).
6. Test [prefix]/Main/two and note that both HomeScreen (InitialRoute) and LinkScreen print to the console log. I would only expect LinkSCreen to print anything.
