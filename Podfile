source 'git@github.com:conichiGMBH/ios-specs.git'
source 'git@github.com:CocoaPods/Specs.git'

platform :ios, '8.0'
use_frameworks!
inhibit_all_warnings!

def reusepods
  # Owned by conichi
  pod 'Conichi_iOSUtilities', '~> 2.0'
  pod 'Conichi_Authentication', '~> 1.0'

  # Objc pods 🎉
  pod 'AFNetworking', '~> 3.0'
  pod 'SVProgressHUD', '~> 2.0'
  pod 'PureLayout', '~> 3.0'
  pod 'pop', '~> 1.0'
  pod 'SDWebImage', '~> 3.7'
  pod 'libextobjc', '~> 0.2'
  pod 'Fabric'
  pod 'Crashlytics'
  pod 'Bolts', '~> 1.2'
  pod 'KZAsserts', '~> 1.0'

  pod 'FastEasyMapping', :git => 'git@github.com:conichiGMBH/FastEasyMapping.git', :branch => 'master'

  # Swift pods 🎉
  pod 'AsyncSwift', '~> 1.0'
  pod 'SwiftyJSON', '~> 2.0'
end

def testpods
  # Objc pods 🎉
  pod 'OHHTTPStubs', '~> 5.0'
  pod 'OCMock', :git => 'https://github.com/conichiGMBH/ocmock.git', :commit => 'e736c922687a79cb9e86139478900f25316df907'
  pod 'FBSnapshotTestCase/Core'

  # Swift pods 🎉
  pod 'Quick'
  pod 'Nimble'
  pod 'Nimble-Snapshots'
  pod 'OHHTTPStubs/Swift', '~> 5.0'
end

target 'ios-merchant-staging' do
  reusepods
  target 'ios-merchant-staging-tests' do
      inherit! :search_paths
      testpods
  end
end

target 'ios-merchant-production' do
  reusepods
  target 'ios-merchant-production-tests' do
      inherit! :search_paths
      testpods
  end
end
