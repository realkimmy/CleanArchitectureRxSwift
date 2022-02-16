# Uncomment the next line to define a global platform for your project
platform :ios, '11.0'
inhibit_all_warnings!

def rx_swift
    pod 'RxSwift', '~> 6.2.0'
end

def rx_cocoa
    pod 'RxCocoa', '~> 6.2.0'
end

def query_kit
  pod 'QueryKit', '~> 0.14.1'
end

def test_pods
    pod 'RxTest', '~> 6.2.0'
    pod 'RxBlocking', '~> 6.2.0'
    pod 'Nimble'
end


target 'CleanArchitectureRxSwift' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!
  rx_cocoa
  rx_swift
  query_kit
  target 'CleanArchitectureRxSwiftTests' do
    inherit! :search_paths
    test_pods
  end

end

target 'CoreDataPlatform' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!
  rx_swift
  query_kit
  target 'CoreDataPlatformTests' do
    inherit! :search_paths
    test_pods
  end

end

target 'Domain' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!
  rx_swift

  target 'DomainTests' do
    inherit! :search_paths
    test_pods
  end

end

target 'NetworkPlatform' do
    # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
    use_frameworks!
    rx_swift
    pod 'Alamofire', '~> 5.4.4'
    pod 'RxAlamofire', '~> 6.1.0'

    target 'NetworkPlatformTests' do
        inherit! :search_paths
        test_pods
    end
    
end

target 'RealmPlatform' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!
  rx_swift
  query_kit
  pod 'RxRealm', '~> 5.0.4'
  pod 'RealmSwift', '~> 10.22.0'
  pod 'Realm', '~> 10.22.0'

  target 'RealmPlatformTests' do
    inherit! :search_paths
    test_pods
  end

end
