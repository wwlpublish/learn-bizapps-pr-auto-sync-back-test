> [!VIDEO https://www.microsoft.com/videoplayer/embed/]

In this section, you'll learn the basics of how testing should be carried out.

## Unit tests

A *unit test* is used to check whether a specific function or feature of your app is working correctly. These tests are repeatable and run programmatically within fractions of a second. In short, unit testing makes sure that the code included within your solution works as expected.

## End-to-end tests

*End-to-end tests* are used to check whether the overall solution runs correctly. This is important because even if all unit tests function correctly, the integration between two units can potentially fail. These tests are done by following a test scenario that's close to the use case of the actual business process.

Although you may end up with a solution that doesn't involve custom code and thus the need for unit testing may not have a great appeal, end-to-end tests will always be a requirement before we turn our solution lose to users within the organization.

## User acceptance tests

A *user acceptance test* (UAT) is done by the user of the app instead of the maker. This test is to ensure that what has been built by the makers matches the requirements initially requested by the user.

Here are some tips for getting good results from UATs:

-   Test with the real users.

-   Try to choose users with diversity in terms of IT skill levels. This way, you can get various feedback.

-   Don't give the user instructions; see whether they can understand the app intuitively.

-   Observe how they navigate the app without assistance, and see where you can improve the design.

-   When the user is stuck on a screen, ask them to explain what their expectation was.

-   Try out different devices to make sure the test cases behave the same.

-   Ideally, test the app in the user's actual environment or location if the app uses offline capabilities.

-   Ask your users to try to "break" your app, such as by entering unusual characters in text fields.

-   Users will typically test the "happy path" (the path a user takes when everything is going perfectly); ask them to also test scenarios such as canceling an expense report instead of submitting it, or denying an expense report instead of approving it.

Your users might not be familiar with testing software. Let them know what kind of feedback you're looking for. It's often helpful to provide a template for "bugs" to make sure testers explain exactly what they were doing, what happened, what they expected to happen instead, and any relevant information about their testing environment (such as device type and browser).

It's natural and OK for the user to request changes to the specifications or ask for other features.

These requests should be recorded in the feature list described in [Prioritizing features and requests](/power-apps/guidance/planning/prioritizing-features/?azure-portal=true).
