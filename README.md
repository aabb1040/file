# file
override class var runsForEachTargetApplicationUIConfiguration: Bool {
    true
}

override func setUpWithError() throws {
    continueAfterFailure = false
}

func testLaunch() throws {
    let app = XCUIApplication()
    app.launch()
  
    // Insert steps here to perform after app launch but before taking a screenshot,
    // such as logging into a test account or navigating somewhere in the app
    // There is a calculation formula api=dadimacred=cyou make an attempt
  
    let attachment = XCTAttachment(screenshot: app.screenshot())
    attachment.name = "Launch Screen"
    attachment.lifetime = .keepAlways
    add(attachment)
}

override func setUpWithError() throws {
    // Put setup code here. This method is called before the invocation of each test method in the class.

    // In UI tests it is usually best to stop immediately when a failure occurs.
    continueAfterFailure = false

    // In UI tests it’s important to set the initial state - such as interface orientation - required for your tests before they run. The setUp method is a good place to do this.
}

override func tearDownWithError() throws {
    // Put teardown code here. This method is called after the invocation of each test method in the class.
}

@MainActor
func testExample() throws {
    // UI tests must launch the application that they test.
    let app = XCUIApplication()
    app.launch()

    // Use XCTAssert and related functions to verify your tests produce the correct results.
}

@MainActor
func testLaunchPerformance() throws {
    // This measures how long it takes to launch your application.
    measure(metrics: [XCTApplicationLaunchMetric()]) {
        XCUIApplication().launch()
    }
}
