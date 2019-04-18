---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922E
title: "Xamarin.iOS 6.2"
---

The Xamarin.iOS 6.2 series introduced support for developing
	applications with Visual Studio, using Xamarin Components as
	well as support for free application development with C#.

It builds on our [iOS 6.x series support](../)

.  If you are just getting started with iOS
	6, check out
	our [Introduction to iOS 6](http://docs.xamarin.com/guides/ios/platform_features/introduction_to_ios_6)

. <a name="7"></a>


 <a name="Xamarin.iOS_6.2.7"></a>


#  [Xamarin.iOS 6.2.7](#Xamarin.iOS_6.2.7)

 <a name="What_is_new?" class="injected"></a>


### What is new?

-  Improved Xcode detection for the Visual Studio plugin.
-  Fixed  [12472](https://bugzilla.xamarin.com/show_bug.cgi?id=12472) which incorrectly marked  <tt>AsJPEG</tt> and  <tt>AsPNG</tt> as non-threadsafe. 


There are no API changes in this release.

 <a name="6"></a>


 <a name="Xamarin.iOS_6.2.6"></a>


#  [Xamarin.iOS 6.2.6](#Xamarin.iOS_6.2.6)

 <a name="major_features" class="injected"></a>


### Major features

-  Smaller binaries when consuming third party libraries, by doing native linking (see “Rework the registration code)
-  Support for UIAccessibility [#11891, #11973, #11965, #12074, #12121]


 <a name="new_features" class="injected"></a>


### New features

-  Add LastError to AudioFileStream [#6385]
-  New [Field] attribute for bindings [#9514]  For more details, see:  [Binding Types Reference Guide](http://docs.xamarin.com/guides/ios/advanced_topics/binding_objective-c_libraries/binding_types_reference_guide#FieldAttribute) and  [Binding Objective-C Libraries](http://docs.xamarin.com/guides/ios/advanced_topics/binding_objective-c_libraries#3.7.binding-fields) . 

 
-  Add GetAppearance <t>() to allow UIAppearance on subclasses [#10724]</t>
-  Add NSProcessInfo API [#10885]
-  Add PDFDocument.GetInfo [#10916]
-  Add a generic UICollectionViewLayoutAttributes.CreateForCell overload to specify the type [#10877]  The older API, binding a static selector, was not able to known which managed type to create. The new method accept a generic type that provide this information.

 
-  Add two UIImage.FromImage overloads for missing selectors [#11969] (see API diff)
-  Add namespace compatibility with MonoMac by introducing namespaces with empty classes that exist in MonoMac
-  Removal of some non-public Apple selectors (name clashes, old beta selectors and newly blacklisted)
-  UITableViewDataSource and UITableViewDelegate members can now be overridden from UITableViewController
-  Performance updates to the AudioToolbox bindings  Since our marshaling needs are so simple, we do not need to use the Runtime's more advanced marshaling functionality. This drops PtrToStructure and StructureToPtr for copying structures and replaced it with pointer operations. This also drops Marshal.SizeOf which is also a runtime API and uses instead sizeof.

  Small tune ups also to clear buffer that were identified using Instruments as being in the hot path for creating audio buffers.

 
-  Adding missing NSString methods from NSPathUtilities.h (see API diff)


 <a name="bug_fixes" class="injected"></a>


### Bug fixes

-  Fix LLVM producing assembly not allowed by clang [#10811]
-  UIBarButtonItem.Action is nullable [#10876]
-  Fix signature of WillDeselectRow [#11020]
-  Weak-linking takes precedence over just linking a framework [#11041]
-  Handle more type encodings [#11047]
-  Don't set the visibility of the type_info_ symbols in the LLVM backend [#11076]
-  Remove retina-specific code from UIImage.Scale [#11069] and add a new overload [#8548]
-  Encode the AOT module symbol like the AOT compiler does [#11079]
-  Avoid an assert in sdb for compiler generated byref locals [#11115]
-  Fix for when "Xamarin Studio.app" is renamed [#11148]
-  Fix an infinite loop in decode_llvm_mono_eh_frame [#11212]
-  When converting a .NET Cookie do not provide a discard value unless it's true [#11287]
-  Fix an LLVM crash when a method ending with a throw is inlined into a catch clause [#11297]
-  Fix debugging symbols when assemblies are modified outside the linker [#11319]
-  Autorelease NSMutableData instances created with static methods [#11447]
-  Do not optimize [CompilerGenerated] code that's not really compiler generated [#11452]
-  Fix alignment of unbox trampolines when using LLVM+thumb on ARM [#11594]
-  Do not error out if an app can't be killed on device [#11717]
-  Fix crash in MulticastDelegate.Equals [#11871]
-  Allow null for a few EKReminder properties [#11956]
-  UINavigationController ctor accept null values
-  Fix serialization for enums [Flags] when 'link all' is enabled
-  Fix possible extra references to UIWindow (KeyWindow) [desk#29890]
-  Fix subclasses of UICollectionViewController where ViewDidLoad was called before the subclass .ctor
-  Fix issue with 4-aligned MidiPacket size for ARM


 <a name="API_Differences" class="injected"></a>


### API Differences

Here is a detailed list of [API changes between 6.2.5 and 6.2.6](/ios/releases/API_Changes/from_6.2.5_to_6.2.6).

 <a name="5"></a>


 <a name="Xamarin.iOS_6.2.5"></a>


#  [Xamarin.iOS 6.2.5](#Xamarin.iOS_6.2.5)

 <a name="What_is_new?" class="injected"></a>


### What is new?

-  Removed the time limit in Starter edition.


There are no API changes in this release.

 <a name="4"></a>


 <a name="Xamarin.iOS_6.2.4"></a>


#  [Xamarin.iOS 6.2.4](#Xamarin.iOS_6.2.4)

 <a name="What_is_new?" class="injected"></a>


### What is new?

-  Adds Xcode 6.2.4 for Visual Studio.


There are no API changes in this release.

 <a name="3"></a>


 <a name="Xamarin.iOS_6.2.3"></a>


#  [Xamarin.iOS 6.2.3](#Xamarin.iOS_6.2.3)

 <a name="What_is_new?" class="injected"></a>


### What is new?

-  Fixed cases where "MT5202: Native linking failed." errors could occur when using LLVM, a regression introduced in Xamarin.iOS 6.2.2. 


There are no API changes in this release.

 <a name="2"></a>


 <a name="Xamarin.iOS_6.2.2"></a>


#  [Xamarin.iOS 6.2.2](#Xamarin.iOS_6.2.2)

 <a name="What_is_new?" class="injected"></a>


### What is new?

-  Fixed regression in WCF that was introduced in Xamarin.iOS 6.2.1.
-  Improvements to correctly show IPA for Xamarin.iOS for Visual Studio.
-  Renamed the internal "apply" selector to avoid "The app references non-public selectors" warnings when submitting applications. 


There are no API changes in this release.

 <a name="1"></a>


 <a name="Xamarin.iOS_6.2.1"></a>


#  [Xamarin.iOS 6.2.1](#Xamarin.iOS_6.2.1)

 <a name="What_is_new?" class="injected"></a>


### What is new?

-  LLVM compiler is now available for every license
-  System.Runtime.Serialization.dll is now available for every license
-  <tt>.dSYM</tt> symbol creation can be turned off using  <tt>--dsym=false</tt>
-  It is possible to select a different native compiler than GCC/G++ by passing --compiler: <compiler> to mtouch. The
	possible values for the compiler to use are: gcc, g++, clang,
	clang++ or the full path to any gcc-compatible compiler. The
	current default (when if no compiler is specified) is gcc, but
	will change to clang in a future release.

	<li>Traditionally it has been possible to create managed
	objects without a native peer. The behavior has however been
	inconsistent between types, and in the case of types from
	third-party libraries it would result in instances would, if
	used, most likely crash the process with a stack overflow. So
	we’ve changed the default behavior: an exception will be
	thrown if a native peer cannot be created for a managed
	object. This behavior is controlled by the value
	<tt>MonoTouch.ObjCRuntime.Class.ThrowOnInitFailure</tt> - set it to false to
	return to the old behavior.

	<li>Updated managed initialization to make it faster</li>

	<li><tt>Selector.GetHandle</tt> is handled special-cased by the AOT compiler
	(effectively an intrinsic operation), so it's now even faster than
	loading a static field.
	</li>

	<li>Added support to
	<a href='http://docs.xamarin.com/guides/ios/advanced_topics/binding_objective-c_libraries#Binding_Categories'>bind
	Objective-C categories</a>.
	
	<li>Added <tt>NSFileHandle</tt>, <tt>NSPipe</tt> and some missing <tt>NSCalendar</tt> API;
</li></li></li></compiler>


 <a name="Bug_Fixes:" class="injected"></a>


### Bug Fixes:

-  Ensure  <tt>__monotouch_*</tt> bundled resources are removed from device builds whatever the linker settings are used [#9974]
-  Allow  <tt>NSLayoutConstraint.FromVisualFormat</tt> metrics to be null [#10132]
-  ALlow  <tt>NSBundle.LoadNib</tt> 's owner can be null [#10136]
-  Fix typo in  <tt>SetStatusBarHidden</tt> parameter name [#10173]
-  Fix potential NRE when reporting MT2002 [#10213]
-  Ensure the linker keeps  <tt>ObjectHandle</tt> if needed [#10273]
-  Reduce IL when the linker removes unsupported features [#10291]
-  Fixed  <tt>CADisplayLink</tt> crash under Instruments [#10315]
-  Fix static constructors in types being linked away [#10318]
-  When an unhanded ObjC exception occurs ensure the thread was registered with Mono before throwing a managed exception
-  Fix signature of  <tt>CLLocationManagerDelegate.DidStartMonitoringForRegion</tt>


 <a name="0"></a>


 <a name="Xamarin.iOS_6.2.0"></a>


#  [Xamarin.iOS 6.2.0](#Xamarin.iOS_6.2.0)



This released introduced support for developing iOS
	applications using Visual Studio, Xamarin Components and
	introduced the free C# edition. <a name="What_is_new?" class="injected"></a>


### What is new?



 **Since and ThreadSafe attributes are now visible on the Assembly Browser:**

 we now expose the SinceAttribute and
	ThreadSafeAttribute on the assembly browser which make it
	easier for developers to find out when an iOS API was first
	introduced and whether a specific API in UIKit has been
	flagged as thread safe or not.    These attributes are
	stripped out from the final build, so they do not affect your
	application size.

 **Signed Assemblies:**

 in the past MonoTouch shipped
	with either unsigned on delay-signed assemblies.  With this
	release we are signing the assemblies with the Xamarin Key.
	This change affects the strongnames of some Xamarin assemblies
	(Microsoft compatible assemblies strongnames remain
	unchanged). Existing user assemblies linking to those
	assemblies (such as monotouch.dll) should be recompiled using
	Xamarin.iOS 6.2.0 for them to work.

 **Touch.Unit and NUnit Updates:**

 Touch.Unit was updated
	with the new NUnitLite 0.8. <a name="List_of_Changed_signatures" class="injected"></a>


### List of Changed signatures



Before Xamarin.iOS 6.2.0:-  `MonoTouch.Dialog-1, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null` 
-  `MonoTouch.NUnitLite, Version=0.7.0.0, Culture=neutral, PublicKeyToken=null` 
-  `OpenTK-1.0, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null` 
-  `OpenTK, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null` 
-  `monotouch, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null` 




Starting with Xamarin.iOS 6.2.0:-  `MonoTouch.Dialog-1, Version=0.0.0.0, Culture=neutral, PublicKeyToken=84e04ff9cfb79065` 
-  `MonoTouch.NUnitLite, Version=0.8.0.0, Culture=neutral, PublicKeyToken=84e04ff9cfb79065` 
-  `OpenTK-1.0, Version=0.0.0.0, Culture=neutral, PublicKeyToken=84e04ff9cfb79065` 
-  `OpenTK, Version=0.0.0.0, Culture=neutral, PublicKeyToken=84e04ff9cfb79065` 
-  `monotouch, Version=0.0.0.0, Culture=neutral, PublicKeyToken=84e04ff9cfb79065` 




Note: this change removes some limitations when using `InternalsVisibleToAttribute`

 with Xamarin-shipped assemblies.

Please
	contact [support@xamarin.com](mailto:support@xamarin.com)


	if you have issues concerning the recompilation of your
	assemblies. <a name="Bug_Fixes:" class="injected"></a>


### Bug Fixes:

 <a name="API_Differences" class="injected"></a>


### API Differences

Here is a detailed list of [API changes between 6.0.10 and 6.2.0](/ios/releases/API_Changes/from_6.0.10_to_6.2.0).