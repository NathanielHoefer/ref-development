tories:
Short descriptions of a small piece of desired functionality, written in the user's language.

Life cycle:
1. Backlog Refinement - Listing stories by priority
2. Planning - Determining how to implement and test
3. Implementation - Producing code and tests
4. Demo - Showing tests and functionality

Types of Stories:
	User Stories
	Primary means of expressing needed functionality, and are value-centric

		Components:
		1. User voice statement
		2. Acceptance criteria
	
		Format:
		As a <user role>, I want to <activity>, so that <business value>.

		Example:
		As a rider, I want to hear acceleration, braking, skidding, and crashing sounds so that I will feel immersed in the ride experience.

	Enabler Stories
	Stories that may not directly touch any end user, but can support exploration, architecture, or infrastructure.

		Components:
		1. Story statement
		2. Acceptance criteria
	
		Example:
		Record or buy some realistic sounds so we can test them with potential users.

		 - Refactoring and Spikes
		 - Building or improving development/deployment infrastructure
		 - Running jobs that require human interaction
		 - Creating required product or component configurations for different purposes
		 - Verification of system qualities (e.g., performance and vulnerability testing)
 
Writing Good Stories (3C's)
 - Card: Capture story on a card of some sort (index card, sticky note, tool)
 - Conversation: A discussion representing a "promise for a conversation" that spans all steps in the story life cycle
 - Confirmation: The acceptance criteria
	- Given: precondition(s) and fixed data
	- When: action and input data
	- Then: postcondition and output data
	
Estimating Stories:
Story points are used to value the story's work and are calculated on the following qualities:
 - Volume - How much is there?
 - Complexity - How hard is it?
 - Knowledge - What's known?
 - Uncertainty - What's unknown?
 
Story Deliverables:
1. Story Acceptance Tests - 
2. Unit tests

Story Template:
	Type:
		[User story|Enabler]
	Story Points:
		<Estimated Value>
	Statement:
		[User voice|Story]
		As a <user role>,
		I want to <action>,
		so that <business value>.
	Acceptance Criteria:
		Given <preconditions>,
		When <action>
		Then <response>.
		<Must pass acceptance tests and unit tests>
