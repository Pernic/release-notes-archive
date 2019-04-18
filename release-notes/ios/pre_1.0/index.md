---
id: 73DBF9B6-589E-75E0-188F-8ED2870F0594
title: "Pre 1.0"
subtitle: "MonoTouch Release Notes:"
---

<a name="1.0_Rc2" class="injected"></a>


### 1.0 Rc2

 <a name="Fixes_in_RC2" class="injected"></a>


# Fixes in RC2

-  In very specific cases, wrappers could be shared improperly between methods leading to a crash. 


 <a name="1.0_Rc" class="injected"></a>


### 1.0 Rc

 <a name="Additions_in_RC" class="injected"></a>


# Additions in RC

-  Added System.Json
-  Added Mono.Security for HTTPS and NTLM
-  Added MonoTouch.Foundation.PreserveAttribute to preserve members from the linker 
-  Added NSObject.BeginInvokeOnMainThread(Selector,NSObject), NSObject.BeginInvokeOnMainThread(NSAction) for the non-waiting behavior of -[NSObject performSelectorOnMainThread:withObject:waitUntilDone] (i.e. when waitUntilDone=NO) 
-  Added CGImage.WithMaskingColors (float [])
-  Added static NSObject.Alloc (Class)
-  Added MediaPlayer binding
-  Added DrawString overloads for UIView
-  Added NSUrlMutableRequest binding
-  Added encoding operations to convert strings to NSData
-  Added NSData to string conversion routines
-  Added NSUrlConnection.SendSynchronousRequest
-  Added NSUrlRequest indexer to retrieve Header values


 <a name="Fixes_in_RC" class="injected"></a>


# Fixes in RC

-  Fixed crash when using -linksdkonly
-  Fixed SpecialFolders.MyDocuments to point to the sandbox/Documents
-  Fixed System.IO.Compression
-  Fixed MapKit binding to allow interchangable use of MKAnnotation and MKPlacemark 
-  Fixed NSBundle.LoadNib to property return an NSArray
-  Fixed Serialization of value type properties
-  Fixed invalid GCHandle storage of deleted objects
-  Fixed alignment error when throwing exceptions in the simulator
-  Fixed static generic context trampoline to not clobber $r1


 <a name="Removals_in_RC" class="injected"></a>


# Removals in RC

-  Removed NSObject.InvokeOnMainThread (Selector, NSObject, bool)


 <a name="Changes_in_RC" class="injected"></a>


# Changes in RC

-  Renamed static CGImage.Copy (CGImage) to instance CGImage.Clone ()
-  Renamed instance CGImage.Copy (CGImage, CGColorSpace) to instance CGImage.WithColorSpace (CGColorSpace) 
-  Renamed static CGImage.FromImageInReck (CGImage, RectangleF) to instance CGImage.WithImageInRect (RectangleF) 
-  Renamed static CGImage.FromImageMask (CGImage, CGImage) to instance CGImage.WithMask (CGImage) 
-  Renamed URL property to Url on NSUrlRequest


 <a name="1.0_Beta_8" class="injected"></a>


### 1.0 Beta 8

 <a name="Additions_in_Beta_8" class="injected"></a>


# Additions in Beta 8

-  added -gcc_flags option to mtouch
-  added NSData.Bytes and NSData.Count
-  added full support for decimal types


 <a name="Fixes_in_Beta_8" class="injected"></a>


# Fixes in Beta 8

-  fixed a bug when linking assemblies with InternalsVisibleTo attributes
-  fixed bug when pinvoke callbacks were called on an unregistered thread
-  fixed TabBarItem to exist on UIViewController
-  fixed compilation on x86 when -ObjC is used
-  fixed NSBundle.LoadNib binding


 <a name="Changes_in_Beta_8" class="injected"></a>


# Changes in Beta 8

-  removed -lib flag from mtouch (use -gcc_flags)


 <a name="1.0_Beta_7" class="injected"></a>


### 1.0 Beta 7

 <a name="Additions_in_Beta_7" class="injected"></a>


# Additions in Beta 7

-  Added NSBundle.LoadNib
-  Added NSBundle.PathForImageResource
-  Added NSBundle.PathForSoundResource
-  Added NSData.FromUrl
-  Added UIImage.FromData
-  Added UITabBarController.TabBarItem


 <a name="Fixes_in_Beta_7" class="injected"></a>


# Fixes in Beta 7

-  Fixed mtouch invocation of the linker for simulator configurations.
-  Fixed UIActionSheet.WillDismiss event.


 <a name="Changes_in_Beta_7" class="injected"></a>


# Changes in Beta 7

-  Removed the OpenTK.Graphics.ES11.GL.LoadAll() and OpenTK.Graphics.ES20.GL.LoadAll() methods. Now to initialize the GL types you must do one of two things: -   Inherit from OpenTK.Platform.iPhoneOS.iPhoneOSGameView, and call either iPhoneOSGameView.CreateFrameBuffer() or iPhoneOSGameView.Run() before using any GL methods. 
-   Call OpenTK.Platform.Utilities.CreateGraphicsContext() before making any GL calls. 


 
-  The GLPaint and OpenGLESSample samples have been updated to use Utilities.CreateGraphicsContext() to initialize GL 
-  New GLPaint-GV and OpenTLESSample-GV samples have been added to use iPhoneOSGameView for comparison 


 <a name="1.0_Beta_6" class="injected"></a>


### 1.0 Beta 6

 <a name="Additions_in_Beta_6" class="injected"></a>


# Additions in Beta 6

-  added experimental System.Xml support


 <a name="Fixes_in_Beta_6" class="injected"></a>


# Fixes in Beta 6

-  fixed long alignment when transitioning to icalls
-  fixed long alignment in managed methods compiled by the cross compiler
-  fixed exception handling when assemblies have been stripped


 <a name="Changes_in_Beta_6" class="injected"></a>


# Changes in Beta 6

-  Updated OpenTK to r2183 (this is a API and ABI change)
-  renamed OpenTK.Graphics.ES11.ES to OpenTK.Graphics.ES11.GL
-  renamed OpenTK.Graphics.ES20.ES to OpenTK.Graphics.ES20.GL


 <a name="1.0_Beta_5" class="injected"></a>


### 1.0 Beta 5

 <a name="Additions_in_Beta_5:" class="injected"></a>


# Additions in Beta 5:

-  added Initial experimental Snow Leopard support.
-  added AVFramework bindings
-  added AddressBook bindings
-  added AddressBookUI bindings
-  added mtouch -lib for linking static native libraries


 <a name="Fixes_in_Beta_5:" class="injected"></a>


# Fixes in Beta 5:

-  fixed null object marshalling
-  fixed Missing selector exception when using PerformSelector / InvokeOnMainThread 
-  fixed Socket problem on device when probing for ipv6 support
-  fixed implicit conversion of null NSStrings
-  fixed UILabel.Text to allow null's
-  fixed mtouch to generate xcodeproj's with the requisite frameworks linked 


 <a name="1.0_Beta_4" class="injected"></a>


### 1.0 Beta 4

 <a name="Fixes_in_Beta_4:" class="injected"></a>


# Fixes in Beta 4:

-  fixed UIAlertView.Messeget typo
-  fixed crash with HttpWebClient.Credentials in NtlmClient
-  fixed #532128, UIBarButtonItem.Clicked not working in some cases
-  fixed #530963, linking issue with virtual generics methods
-  fixed #531955, full-aot crash when using Dictionary&lt;int,int&gt;
-  fixed #532120, full-aot crash working with String[]


 <a name="1.0_Beta_3" class="injected"></a>


### 1.0 Beta 3

 <a name="Additions_in_Beta_3:" class="injected"></a>


# Additions in Beta 3:

-  added bindings for NSAutoreleasePool
-  add moutch --version command
-  added bindings to StoreKit
-  added bindings to SystemConfiguration
-  Add NSObject.InvokeOnMainThread () bindings.


 <a name="Fixes_in_Beta_3:" class="injected"></a>


# Fixes in Beta 3:

-  fixed alwaysBounceHorizontal typo
-  fixed #530807 (typo in UITableView)
-  fixed UIView.MovedToSuperview typo
-  fixed alignment of doubles in the cross compiler
-  Improve documentation import run at installation time
-  fixed generic interface thunk code to not clobber IP register
-  fixed LINQ iterators with value types
-  fixed linking of GenericComparer&lt;&gt; (#530961)
-  fixed null argument handling in runtime marshaller
-  fixed stackoverflow in PerformSelector call


 []()

 <a name="1.0_Beta_2" class="injected"></a>


### 1.0 Beta 2

 <a name="Additions_in_Beta_2:" class="injected"></a>


# Additions in Beta 2:

-  Added a -linksdkonly parameter to mtouch to link only the sdk and preserve the user assemblies. 


 <a name="Fixes_in_Beta_2:" class="injected"></a>


# Fixes in Beta 2:

-  Microsoft.Win32 namespace was too aggressively linked.
-  HttpRequestCreator and friends (Ftp, File) were missing their constructors. 
-  mtouch was not properly reporting missing assemblies.
-  mtouch was not resolving references recursively.
-  mtouch now takes only one assembly, the other have to be specified by -r. 
-  Fixed WebRequest authentication.
-  mtouch now signs the SDK assemblies.
-  Fixed a linker bug wrt virtual methods implementing interfaces and override a method defined in a base class. 
-  Fixed a linker bg wrt virtual methods implementing generic interfaces.
-  Fixed a mtouch bug where arguments were not properly quoted when aot compiling the assemblies. 
-  Fixed -framework linking when using things .
-  Improved imported documentation (properties now imported, etc.).


 <a name="1.0_Beta_1" class="injected"></a>


### 1.0 Beta 1

Initial Release.
