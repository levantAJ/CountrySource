[![Pod Version](https://cocoapod-badges.herokuapp.com/v/CountryKit/badge.png)](http://cocoadocs.org/docsets/CountryKit/)
[![Pod Platform](https://cocoapod-badges.herokuapp.com/p/CountryKit/badge.png)](http://cocoadocs.org/docsets/CountryKit/)
[![Pod License](https://cocoapod-badges.herokuapp.com/l/CountryKit/badge.png)](https://www.apache.org/licenses/LICENSE-2.0.html)

# CountryKit
List of all countries in the world (name, code, phone code)

<img src="https://user-images.githubusercontent.com/6329656/96357601-3b870300-1128-11eb-9091-f98cf9a93924.jpeg" width="300"> <img src="https://user-images.githubusercontent.com/6329656/96357606-4e99d300-1128-11eb-9eee-2d889ca0ed60.jpeg" width="300">

## Requirements

- iOS 9.0 or later
- Xcode 11.0 or later

## Install

### Installation with CocoaPods

```ruby
pod 'CountryKit', '1.0'
```

### Build Project

At this point your workspace should build without error. If you are having problem, post to the Issue and the
community can help you solve it.

## How to use:

```swift
import CountryKit
```

#### Get current country:

```swift
countryKit.currentCountry { result in
    switch result {
    case .success(let country):
        print(country.code, country.name, country.dialCode)
    case .failure(let error):
        print(error)
    }
```

#### Get all countries

```swift
CountryKit().allCountries { result in
    switch result {
    case .success(let countries):
        print(countries)
    case .failure(let error):
        print(error)            
    }
}
```

## Author
- [Tai Le](https://github.com/levantAJ)

## Communication
- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.
- If you **want to contribute**, submit a pull request.


## Licenses

All source code is licensed under the [MIT License](https://raw.githubusercontent.com/levantAJ/CountryKit/master/LICENSE).

