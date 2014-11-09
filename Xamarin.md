### Xamarin

http://xamarin.com/getting-started/android


Run with Ios debugger


What they like
1.	Await/async and asynchrony/responsiveness in general.
2.	Nuget packages, such as Microsoft HTTP Client Libraries and Microsoft Async.
3.	LINQ, especially using the fluent syntax (method chaining).
4.	Meaningful class, method, parameter and variable names.
5.	Interfaces, abstraction, KISS, DRY and SOLID principles.



http://developer.xamarin.com/guides/android/application_fundamentals/resources_in_android/part_1_-_android_resource_basics/



Code Improvements

I performed code improvements in the application. Only the Android version is enhanced, the IOS uses a code similar to the old version.


Added
System.Json
Json.Net
Microsoft Async



Improvements

- Externalized the RSS url list in a resource file. Reason: data should be externalized, so we can add other RSS sources without changing code.

Changes

LVL.Exam.Droid.MainActivity: removed RSS feed names

LVL.Exam.iOS.Helper: removed RSS feed uris, created a high level  

did not use dictionary to store rss because will make ios refactorings more difficult in the future
see value tys as dictionary keys in:
http://developer.xamarin.com/guides/ios/advanced_topics/limitations/

Json
http://forums.xamarin.com/discussion/25634/best-way-to-iterate-a-json-string-for-ios-android-and-wp
http://stackoverflow.com/questions/16338917/iterating-through-json-using-system-json
http://stackoverflow.com/questions/11132288/iterating-over-json-object-in-c-sharp


http://stackoverflow.com/questions/11581101/c-sharp-convert-liststring-to-dictionarystring-string



http://developer.xamarin.com/guides/android/application_fundamentals/resources_in_android/part_6_-_using_android_assets/





	Reading CSV
	http://components.xamarin.com/view/json.net/
	http://shitmores.blogspot.com/2011/01/android-using-csv-file-as.html


http://stackoverflow.com/questions/6349759/using-json-file-in-android-app-resources





1 - Await/async: need to move RSS data load to another thread

Skipped 127 frames!  The application may be doing too much work on its main thread.


http://developer.xamarin.com/guides/android/application_fundamentals/services/
http://developer.xamarin.com/guides/cross-platform/advanced/async_support_overview/
http://developer.xamarin.com/guides/cross-platform/application_fundamentals/nuget_walkthrough/

Options:
- Started Service: more Android like
- Async Programming


- correct date
ri.Published = DateTime.ParseExact (dateStr, "ddd, dd MMM yyyy HH:mm:ss K", new CultureInfo ("en-US")); 

					ri.Published = DateTime.ParseExact (dateStr, "ddd, dd MMM yyyy HH:mm:ss zzz", 
						DateTimeFormatInfo.InvariantInfo,DateTimeStyles.None );

						

