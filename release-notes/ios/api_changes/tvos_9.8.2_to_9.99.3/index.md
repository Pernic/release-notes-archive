---
id: B484D928-ED4A-4E95-8F6A-9EA274DBFA07
title: "tvOS 9.8.2 to 9.99.3"
---

# API diff

 [mscorlib.dll](#diff/xi/Xamarin.TVOS/mscorlib.html)

   


 [System.dll](#diff/xi/Xamarin.TVOS/System.html)

   


 [System.Core.dll](#diff/xi/Xamarin.TVOS/System.Core.html)

   


 [System.Data.dll](#diff/xi/Xamarin.TVOS/System.Data.html)

   


 [System.ServiceModel.dll](#diff/xi/Xamarin.TVOS/System.ServiceModel.html)

   


 [System.Transactions.dll](#diff/xi/Xamarin.TVOS/System.Transactions.html)

   


 [Xamarin.TVOS.dll](#diff/xi/Xamarin.TVOS/Xamarin.TVOS.html)

   


 [MonoTouch.NUnitLite.dll](#diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html)

   


 [System.Net.Http.dll](#diff/xi/Xamarin.TVOS/System.Net.Http.html)

   


   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/mscorlib.html'>mscorlib.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Microsoft.Win32 --> <div> 
<h2>Namespace Microsoft.Win32</h2>
<!-- start type RegistryKey --> <div>
<h3>Type Changed: Microsoft.Win32.RegistryKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public SafeHandles.SafeRegistryHandle Handle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int SubKeyCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int ValueCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public RegistryView View { get; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static object GetValue (string keyName, string valueName, object defaultValue);</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, bool writable);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey CreateSubKey (string subkey, bool writable, RegistryOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKey (string subkey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKey (string subkey, bool throwOnMissingSubKey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKeyTree (string subkey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteSubKeyTree (string subkey, bool throwOnMissingSubKey);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteValue (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public void DeleteValue (string name, bool throwOnMissingValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Flush ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey FromHandle (SafeHandles.SafeRegistryHandle handle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey FromHandle (SafeHandles.SafeRegistryHandle handle, RegistryView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetSubKeyNames ();</span>
	<span class='added added-method ' data-is-non-breaking="">public object GetValue (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public object GetValue (string name, object defaultValue, RegistryValueOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryValueKind GetValueKind (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public string[] GetValueNames ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static RegistryKey OpenBaseKey (RegistryHive hKey, RegistryView view);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey OpenSubKey (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public RegistryKey OpenSubKey (string name, System.Security.AccessControl.RegistryRights rights);</span>
</pre>
</div>

</div> <!-- end type RegistryKey -->

</div> <!-- end namespace Microsoft.Win32 -->
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type AppContext --> <div>
<h3>Type Changed: System.AppContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static string BaseDirectory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string TargetFrameworkName { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static object GetData (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetSwitch (string switchName, bool isEnabled);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool TryGetSwitch (string switchName, out bool isEnabled);</span>
</pre>
</div>

</div> <!-- end type AppContext -->
<!-- start type Console --> <div>
<h3>Type Changed: System.Console</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static ConsoleColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int BufferHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int BufferWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool CapsLock { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int CursorLeft { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int CursorSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int CursorTop { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool CursorVisible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static ConsoleColor ForegroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsErrorRedirected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsInputRedirected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsOutputRedirected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool KeyAvailable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int LargestWindowHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int LargestWindowWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool NumberLock { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static string Title { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool TreatControlCAsInput { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowLeft { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowTop { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static int WindowWidth { get; set; }</span>
</pre>
</div>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event ConsoleCancelEventHandler CancelKeyPress;</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void Beep ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Beep (int frequency, int duration);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void Clear ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MoveBufferArea (int sourceLeft, int sourceTop, int sourceWidth, int sourceHeight, int targetLeft, int targetTop);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void MoveBufferArea (int sourceLeft, int sourceTop, int sourceWidth, int sourceHeight, int targetLeft, int targetTop, char sourceChar, ConsoleColor sourceForeColor, ConsoleColor sourceBackColor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ConsoleKeyInfo ReadKey ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static ConsoleKeyInfo ReadKey (bool intercept);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ResetColor ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetBufferSize (int width, int height);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetCursorPosition (int left, int top);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetWindowPosition (int left, int top);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetWindowSize (int width, int height);</span>
</pre>
</div>

</div> <!-- end type Console -->

</div> <!-- end namespace System -->
<!-- start namespace System.Diagnostics --> <div> 
<h2>Namespace System.Diagnostics</h2>
<!-- start type StackTrace --> <div>
<h3>Type Changed: System.Diagnostics.StackTrace</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void GetFullNameForStackTrace (System.Text.StringBuilder sb, System.Reflection.MethodBase mi);</span>
</pre>
</div>

</div> <!-- end type StackTrace -->

</div> <!-- end namespace System.Diagnostics -->
<!-- start namespace System.Diagnostics.Tracing --> <div> 
<h2>Namespace System.Diagnostics.Tracing</h2>
<!-- start type EventAttribute --> <div>
<h3>Type Changed: System.Diagnostics.Tracing.EventAttribute</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public EventActivityOptions ActivityOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventChannel Channel { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Message { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventOpcode Opcode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventTags Tags { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EventTask Task { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public byte Version { get; set; }</span>
</pre>
</div>

</div> <!-- end type EventAttribute -->
<!-- start type EventSource --> <div>
<h3>Type Changed: System.Diagnostics.Tracing.EventSource</h3>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;EventCommandEventArgs&gt; EventCommandExecuted;</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static string GenerateManifest (System.Type eventSourceType, string assemblyPathToIncludeInManifest);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GenerateManifest (System.Type eventSourceType, string assemblyPathToIncludeInManifest, EventManifestOptions flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Guid GetGuid (System.Type eventSourceType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string GetName (System.Type eventSourceType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;EventSource&gt; GetSources ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SendCommand (EventSource eventSource, EventCommand command, System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; commandArguments);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetCurrentThreadActivityId (System.Guid activityId);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetCurrentThreadActivityId (System.Guid activityId, out System.Guid oldActivityThatWillContinue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Write (string eventName, EventSourceOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void WriteEventCore (int eventId, int eventDataCount, EventSource.EventData* data);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void WriteEventWithRelatedActivityId (int eventId, System.Guid relatedActivityId, object[] args);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void WriteEventWithRelatedActivityIdCore (int eventId, System.Guid* relatedActivityId, int eventDataCount, EventSource.EventData* data);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~EventSource ();</span>
</pre>
</div>

</div> <!-- end type EventSource -->

</div> <!-- end namespace System.Diagnostics.Tracing -->
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<!-- start type DirectoryInfo --> <div>
<h3>Type Changed: System.IO.DirectoryInfo</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Serialization.ISerializable</span>
</pre>
</div>

</div> <!-- end type DirectoryInfo -->
<!-- start type File --> <div>
<h3>Type Changed: System.IO.File</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static FileStream Create (string path, int bufferSize, FileOptions options);</span>
</pre>
</div>

</div> <!-- end type File -->
<!-- start type FileInfo --> <div>
<h3>Type Changed: System.IO.FileInfo</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Serialization.ISerializable</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public FileInfo Replace (string destinationFileName, string destinationBackupFileName);</span>
	<span class='added added-method ' data-is-non-breaking="">public FileInfo Replace (string destinationFileName, string destinationBackupFileName, bool ignoreMetadataErrors);</span>
</pre>
</div>

</div> <!-- end type FileInfo -->
<!-- start type FileSystemInfo --> <div>
<h3>Type Changed: System.IO.FileSystemInfo</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.Runtime.Serialization.ISerializable</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);</span>
</pre>
</div>

</div> <!-- end type FileSystemInfo -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.Runtime.CompilerServices --> <div> 
<h2>Namespace System.Runtime.CompilerServices</h2>
<!-- start type ConditionalWeakTable`2 --> <div>
<h3>Type Changed: System.Runtime.CompilerServices.ConditionalWeakTable`2</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~ConditionalWeakTable ();</span>
</pre>
</div>

</div> <!-- end type ConditionalWeakTable`2 -->

</div> <!-- end namespace System.Runtime.CompilerServices -->
<!-- start namespace System.Runtime.InteropServices --> <div> 
<h2>Namespace System.Runtime.InteropServices</h2>
<!-- start type ExternalException --> <div>
<h3>Type Changed: System.Runtime.InteropServices.ExternalException</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type ExternalException -->
<!-- start type Marshal --> <div>
<h3>Type Changed: System.Runtime.InteropServices.Marshal</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool AreComObjectsAvailableForCleanup ();</span>
</pre>
</div>

</div> <!-- end type Marshal -->

</div> <!-- end namespace System.Runtime.InteropServices -->
<!-- start namespace System.Security --> <div> 
<h2>Namespace System.Security</h2>
<!-- start type CodeAccessPermission --> <div>
<h3>Type Changed: System.Security.CodeAccessPermission</h3>
<p>Modified methods:</p>
<pre>
<div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void Assert ()
</div><div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void Demand ()
</div><div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void Deny ()
</div><div data-is-breaking="">	public <span class='removed removed-inline removed-breaking-inline'>virtual</span> <span class='removed removed-inline '>final</span> void PermitOnly ()
</div></pre>

</div> <!-- end type CodeAccessPermission -->

</div> <!-- end namespace System.Security -->
<!-- start namespace System.Security.AccessControl --> <div> 
<h2>Namespace System.Security.AccessControl</h2>
<!-- start type AuthorizationRuleCollection --> <div>
<h3>Type Changed: System.Security.AccessControl.AuthorizationRuleCollection</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AuthorizationRuleCollection ();</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddRule (AuthorizationRule rule);</span>
</pre>
</div>

</div> <!-- end type AuthorizationRuleCollection -->
<!-- start type CommonSecurityDescriptor --> <div>
<h3>Type Changed: System.Security.AccessControl.CommonSecurityDescriptor</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddDiscretionaryAcl (byte revision, int trusted);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddSystemAcl (byte revision, int trusted);</span>
</pre>
</div>

</div> <!-- end type CommonSecurityDescriptor -->
<!-- start type DiscretionaryAcl --> <div>
<h3>Type Changed: System.Security.AccessControl.DiscretionaryAcl</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAccess (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool RemoveAccess (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAccessSpecific (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAccess (AccessControlType accessType, System.Security.Principal.SecurityIdentifier sid, ObjectAccessRule rule);</span>
</pre>
</div>

</div> <!-- end type DiscretionaryAcl -->
<!-- start type ObjectSecurity --> <div>
<h3>Type Changed: System.Security.AccessControl.ObjectSecurity</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected ObjectSecurity ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected ObjectSecurity (CommonSecurityDescriptor securityDescriptor);</span>
</pre>
</div>

</div> <!-- end type ObjectSecurity -->
<!-- start type SystemAcl --> <div>
<h3>Type Changed: System.Security.AccessControl.SystemAcl</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void AddAudit (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool RemoveAudit (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveAuditSpecific (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetAudit (System.Security.Principal.SecurityIdentifier sid, ObjectAuditRule rule);</span>
</pre>
</div>

</div> <!-- end type SystemAcl -->

</div> <!-- end namespace System.Security.AccessControl -->
<!-- start namespace System.Security.Principal --> <div> 
<h2>Namespace System.Security.Principal</h2>
<!-- start type WindowsIdentity --> <div>
<h3>Type Changed: System.Security.Principal.WindowsIdentity</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void RunImpersonated (Microsoft.Win32.SafeHandles.SafeAccessTokenHandle safeAccessTokenHandle, System.Action action);</span>
	<span class='added added-method ' data-is-non-breaking="">public static T RunImpersonated&lt;T&gt; (Microsoft.Win32.SafeHandles.SafeAccessTokenHandle safeAccessTokenHandle, System.Func&lt;T&gt; func);</span>
</pre>
</div>

</div> <!-- end type WindowsIdentity -->

</div> <!-- end namespace System.Security.Principal -->
<!-- start namespace System.Threading --> <div> 
<h2>Namespace System.Threading</h2>
<!-- start type EventWaitHandle --> <div>
<h3>Type Changed: System.Threading.EventWaitHandle</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool explicitDisposing);</span>
</pre>
</div>

</div> <!-- end type EventWaitHandle -->

</div> <!-- end namespace System.Threading -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/System.html'>System.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Mono.Security.Interface --> <div> 
<h2>Namespace Mono.Security.Interface</h2>
<!-- start type MonoTlsProviderFactory --> <div>
<h3>Type Changed: Mono.Security.Interface.MonoTlsProviderFactory</h3>
<p>Removed field:</p>

<pre>
	<span class='removed removed-field breaking' data-is-breaking="">public static MonoTlsProviderFactoryDelegate _PrivateFactoryDelegate;</span>
</pre>

</div> <!-- end type MonoTlsProviderFactory -->
<h3>Removed Type <span class='breaking' data-is-breaking="">Mono.Security.Interface.MonoTlsProviderFactoryDelegate</span></h3>
</div> <!-- end namespace Mono.Security.Interface -->
<!-- start namespace System --> <div> 
<h2>Namespace System</h2>
<!-- start type Uri --> <div>
<h3>Type Changed: System.Uri</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string IdnHost { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("The method has been deprecated. It is not used by the system. http://go.microsoft.com/fwlink/?linkid=14202")]
	protected virtual void Canonicalize ();</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("The method has been deprecated. It is not used by the system. http://go.microsoft.com/fwlink/?linkid=14202")]
	protected virtual void CheckSecurity ();</span>
</pre>
</div>

</div> <!-- end type Uri -->
<!-- start type UriParser --> <div>
<h3>Type Changed: System.UriParser</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual string GetComponents (Uri uri, UriComponents components, UriFormat format)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual void InitializeAndValidate (Uri uri, out UriFormatException parsingError)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual bool IsBaseOf (Uri baseUri, Uri relativeUri)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual bool IsWellFormedOriginalString (Uri uri)
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual UriParser OnNewUri ()
</div><div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> virtual string Resolve (Uri baseUri, Uri relativeUri, out UriFormatException parsingError)
</div></pre>

</div> <!-- end type UriParser -->
<div> <!-- start type GopherStyleUriParser -->
<h3>New Type System.GopherStyleUriParser</h3>
<pre class='added' data-is-non-breaking="">
public class GopherStyleUriParser : System.UriParser {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GopherStyleUriParser ();</span>
}
</pre>
</div> <!-- end type GopherStyleUriParser -->
<div> <!-- start type LdapStyleUriParser -->
<h3>New Type System.LdapStyleUriParser</h3>
<pre class='added' data-is-non-breaking="">
public class LdapStyleUriParser : System.UriParser {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LdapStyleUriParser ();</span>
}
</pre>
</div> <!-- end type LdapStyleUriParser -->

</div> <!-- end namespace System -->
<!-- start namespace System.Diagnostics --> <div> 
<h2>Namespace System.Diagnostics</h2>
<!-- start type Process --> <div>
<h3>Type Changed: System.Diagnostics.Process</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeProcessHandle SafeHandle { get; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">protected override void ~Process ();</span>
</pre>

</div> <!-- end type Process -->
<!-- start type ProcessModuleCollection --> <div>
<h3>Type Changed: System.Diagnostics.ProcessModuleCollection</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public ProcessModule Item { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (ProcessModule module);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (ProcessModule[] array, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public int IndexOf (ProcessModule module);</span>
</pre>
</div>

</div> <!-- end type ProcessModuleCollection -->
<!-- start type ProcessModuleCollectionBase --> <div>
<h3>Type Changed: System.Diagnostics.ProcessModuleCollectionBase</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.IEnumerator GetEnumerator ();</span>
</pre>
</div>

</div> <!-- end type ProcessModuleCollectionBase -->
<!-- start type ProcessStartInfo --> <div>
<h3>Type Changed: System.Diagnostics.ProcessStartInfo</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public ProcessStartInfo (string <span class='removed removed-inline '>filename</span> <span class='added '>fileName</span>)
</div><div data-is-non-breaking="">	public ProcessStartInfo (string <span class='removed removed-inline '>filename</span> <span class='added '>fileName</span>, string arguments)
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IDictionary&lt;System.String,System.String&gt; Environment { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string PasswordInClearText { get; set; }</span>
</pre>
</div>

</div> <!-- end type ProcessStartInfo -->
<!-- start type ProcessThreadCollection --> <div>
<h3>Type Changed: System.Diagnostics.ProcessThreadCollection</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public ProcessThread Item { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public int Add (ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public void CopyTo (ProcessThread[] array, int index);</span>
	<span class='added added-method ' data-is-non-breaking="">public int IndexOf (ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Insert (int index, ProcessThread thread);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Remove (ProcessThread thread);</span>
</pre>
</div>

</div> <!-- end type ProcessThreadCollection -->
<!-- start type ProcessThreadCollectionBase --> <div>
<h3>Type Changed: System.Diagnostics.ProcessThreadCollectionBase</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.IEnumerator GetEnumerator ();</span>
</pre>
</div>

</div> <!-- end type ProcessThreadCollectionBase -->

</div> <!-- end namespace System.Diagnostics -->
<!-- start namespace System.IO --> <div> 
<h2>Namespace System.IO</h2>
<!-- start type FileSystemWatcher --> <div>
<h3>Type Changed: System.IO.FileSystemWatcher</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.IDisposable</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type FileSystemWatcher -->

</div> <!-- end namespace System.IO -->
<!-- start namespace System.Net --> <div> 
<h2>Namespace System.Net</h2>
<!-- start type FileWebResponse --> <div>
<h3>Type Changed: System.Net.FileWebResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool SupportsHeaders { get; }</span>
</pre>
</div>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='removed removed-method breaking' data-is-breaking="">protected override void ~FileWebResponse ();</span>
</pre>

</div> <!-- end type FileWebResponse -->
<!-- start type FtpWebResponse --> <div>
<h3>Type Changed: System.Net.FtpWebResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool SupportsHeaders { get; }</span>
</pre>
</div>

</div> <!-- end type FtpWebResponse -->
<!-- start type HttpWebResponse --> <div>
<h3>Type Changed: System.Net.HttpWebResponse</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public override bool SupportsHeaders { get; }</span>
</pre>
</div>

</div> <!-- end type HttpWebResponse -->
<!-- start type IPAddress --> <div>
<h3>Type Changed: System.Net.IPAddress</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool IsIPv4MappedToIPv6 { get; }</span>
</pre>
</div>

</div> <!-- end type IPAddress -->
<!-- start type TransportContext --> <div>
<h3>Type Changed: System.Net.TransportContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.IEnumerable&lt;System.Security.Authentication.ExtendedProtection.TokenBinding&gt; GetTlsTokenBindings ();</span>
</pre>
</div>

</div> <!-- end type TransportContext -->

</div> <!-- end namespace System.Net -->
<!-- start namespace System.Net.NetworkInformation --> <div> 
<h2>Namespace System.Net.NetworkInformation</h2>
<!-- start type GatewayIPAddressInformationCollection --> <div>
<h3>Type Changed: System.Net.NetworkInformation.GatewayIPAddressInformationCollection</h3>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='removed removed-inline '>protected</span> <span class='added '>protected</span> GatewayIPAddressInformationCollection ()
</div></pre>

</div> <!-- end type GatewayIPAddressInformationCollection -->
<!-- start type IPGlobalProperties --> <div>
<h3>Type Changed: System.Net.NetworkInformation.IPGlobalProperties</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginGetUnicastAddresses (System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UnicastIPAddressInformationCollection EndGetUnicastAddresses (System.IAsyncResult asyncResult);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UnicastIPAddressInformationCollection GetUnicastAddresses ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;UnicastIPAddressInformationCollection&gt; GetUnicastAddressesAsync ();</span>
</pre>
</div>

</div> <!-- end type IPGlobalProperties -->
<!-- start type IPv6InterfaceProperties --> <div>
<h3>Type Changed: System.Net.NetworkInformation.IPv6InterfaceProperties</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual long GetScopeId (ScopeLevel scopeLevel);</span>
</pre>
</div>

</div> <!-- end type IPv6InterfaceProperties -->
<!-- start type NetworkInformationException --> <div>
<h3>Type Changed: System.Net.NetworkInformation.NetworkInformationException</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Exception</span> <span class='added '>System.ComponentModel.Win32Exception</span>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected NetworkInformationException (System.Runtime.Serialization.SerializationInfo serializationInfo, System.Runtime.Serialization.StreamingContext streamingContext);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>override</span> int ErrorCode { get; }
</div></pre>

</div> <!-- end type NetworkInformationException -->
<!-- start type NetworkInterface --> <div>
<h3>Type Changed: System.Net.NetworkInformation.NetworkInterface</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> string Description { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> string Id { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> bool IsReceiveOnly { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> string Name { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> NetworkInterfaceType NetworkInterfaceType { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> OperationalStatus OperationalStatus { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> long Speed { get; }
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> bool SupportsMulticast { get; }
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static int IPv6LoopbackInterfaceIndex { get; }</span>
</pre>
</div>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public static System.Net.IPAddress GetNetMask (System.Net.IPAddress address);</span>
</pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> IPInterfaceProperties GetIPProperties ()
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> IPv4InterfaceStatistics GetIPv4Statistics ()
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> PhysicalAddress GetPhysicalAddress ()
</div><div data-is-non-breaking="">	public <span class='removed removed-inline '>abstract</span> <span class='added '>virtual</span> bool Supports (NetworkInterfaceComponent networkInterfaceComponent)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual IPInterfaceStatistics GetIPStatistics ();</span>
</pre>
</div>

</div> <!-- end type NetworkInterface -->
<!-- start type NetworkInterfaceType --> <div>
<h3>Type Changed: System.Net.NetworkInformation.NetworkInterfaceType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Wman = 237,</span>
	<span class='added added-field ' data-is-non-breaking="">Wwanpp = 243,</span>
	<span class='added added-field ' data-is-non-breaking="">Wwanpp2 = 244,</span>
</pre>
</div>

</div> <!-- end type NetworkInterfaceType -->
<div> <!-- start type NetworkInformationPermission -->
<h3>New Type System.Net.NetworkInformation.NetworkInformationPermission</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class NetworkInformationPermission : System.Security.CodeAccessPermission, System.Security.IPermission, System.Security.ISecurityEncodable, System.Security.IStackWalk, System.Security.Permissions.IUnrestrictedPermission {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NetworkInformationPermission (NetworkInformationAccess access);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NetworkInformationPermission (System.Security.Permissions.PermissionState state);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NetworkInformationAccess Access { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddPermission (NetworkInformationAccess access);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission Copy ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override void FromXml (System.Security.SecurityElement securityElement);</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission Intersect (System.Security.IPermission target);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool IsSubsetOf (System.Security.IPermission target);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsUnrestricted ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.SecurityElement ToXml ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission Union (System.Security.IPermission target);</span>
}
</pre>
</div> <!-- end type NetworkInformationPermission -->
<div> <!-- start type NetworkInformationPermissionAttribute -->
<h3>New Type System.Net.NetworkInformation.NetworkInformationPermissionAttribute</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public sealed class NetworkInformationPermissionAttribute : System.Security.Permissions.CodeAccessSecurityAttribute {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NetworkInformationPermissionAttribute (System.Security.Permissions.SecurityAction action);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public string Access { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public override System.Security.IPermission CreatePermission ();</span>
}
</pre>
</div> <!-- end type NetworkInformationPermissionAttribute -->

</div> <!-- end namespace System.Net.NetworkInformation -->
<!-- start namespace System.Net.Security --> <div> 
<h2>Namespace System.Net.Security</h2>
<!-- start type NegotiateStream --> <div>
<h3>Type Changed: System.Net.Security.NegotiateStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, string targetName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, string targetName, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel allowedImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsClientAsync (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ChannelBinding binding, string targetName, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel allowedImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Net.NetworkCredential credential, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel requiredImpersonationLevel);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AuthenticateAsServerAsync (System.Net.NetworkCredential credential, System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy policy, ProtectionLevel requiredProtectionLevel, System.Security.Principal.TokenImpersonationLevel requiredImpersonationLevel);</span>
</pre>
</div>

</div> <!-- end type NegotiateStream -->
<!-- start type SslStream --> <div>
<h3>Type Changed: System.Net.Security.SslStream</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SslStream (System.IO.Stream innerStream, bool leaveInnerStreamOpen, RemoteCertificateValidationCallback userCertificateValidationCallback, LocalCertificateSelectionCallback userCertificateSelectionCallback, EncryptionPolicy encryptionPolicy);</span>
</pre>
</div>

</div> <!-- end type SslStream -->

</div> <!-- end namespace System.Net.Security -->
<!-- start namespace System.Net.Sockets --> <div> 
<h2>Namespace System.Net.Sockets</h2>
<!-- start type Socket --> <div>
<h3>Type Changed: System.Net.Sockets.Socket</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void CancelConnectAsync (SocketAsyncEventArgs e);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool ConnectAsync (SocketType socketType, ProtocolType protocolType, SocketAsyncEventArgs e);</span>
</pre>
</div>

</div> <!-- end type Socket -->
<!-- start type SocketAsyncEventArgs --> <div>
<h3>Type Changed: System.Net.Sockets.SocketAsyncEventArgs</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public IPPacketInformation ReceiveMessageFromPacketInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SendPacketsElement[] SendPacketsElements { get; set; }</span>
</pre>
</div>

</div> <!-- end type SocketAsyncEventArgs -->
<!-- start type TcpClient --> <div>
<h3>Type Changed: System.Net.Sockets.TcpClient</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
</pre>
</div>

</div> <!-- end type TcpClient -->
<!-- start type UdpClient --> <div>
<h3>Type Changed: System.Net.Sockets.UdpClient</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
</pre>
</div>

</div> <!-- end type UdpClient -->

</div> <!-- end namespace System.Net.Sockets -->
<!-- start namespace System.Security.Authentication.ExtendedProtection --> <div> 
<h2>Namespace System.Security.Authentication.ExtendedProtection</h2>
<!-- start type ServiceNameCollection --> <div>
<h3>Type Changed: System.Security.Authentication.ExtendedProtection.ServiceNameCollection</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Contains (string searchServiceName);</span>
</pre>
</div>

</div> <!-- end type ServiceNameCollection -->
<div> <!-- start type TokenBinding -->
<h3>New Type System.Security.Authentication.ExtendedProtection.TokenBinding</h3>
<pre class='added' data-is-non-breaking="">
public class TokenBinding {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public TokenBindingType BindingType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetRawTokenBindingId ();</span>
}
</pre>
</div> <!-- end type TokenBinding -->
<div> <!-- start type TokenBindingType -->
<h3>New Type System.Security.Authentication.ExtendedProtection.TokenBindingType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TokenBindingType {
	<span class='added added-field ' data-is-non-breaking="">Provided = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Referred = 1,</span>
}
</pre>
</div> <!-- end type TokenBindingType -->

</div> <!-- end namespace System.Security.Authentication.ExtendedProtection -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type Oid --> <div>
<h3>Type Changed: System.Security.Cryptography.Oid</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Oid FromFriendlyName (string friendlyName, OidGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Oid FromOidValue (string oidValue, OidGroup group);</span>
</pre>
</div>

</div> <!-- end type Oid -->

</div> <!-- end namespace System.Security.Cryptography -->
<!-- start namespace System.Security.Cryptography.X509Certificates --> <div> 
<h2>Namespace System.Security.Cryptography.X509Certificates</h2>
<!-- start type X509Chain --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509Chain</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeX509ChainHandle SafeHandle { get; }</span>
</pre>
</div>

</div> <!-- end type X509Chain -->
<!-- start type X509ChainStatusFlags --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509ChainStatusFlags</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">ExplicitDistrust = 67108864,</span>
	<span class='added added-field ' data-is-non-breaking="">HasNotSupportedCriticalExtension = 134217728,</span>
	<span class='added added-field ' data-is-non-breaking="">HasWeakSignature = 1048576,</span>
</pre>
</div>

</div> <!-- end type X509ChainStatusFlags -->
<!-- start type X509Store --> <div>
<h3>Type Changed: System.Security.Cryptography.X509Certificates.X509Store</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">System.IDisposable</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
</pre>
</div>

</div> <!-- end type X509Store -->

</div> <!-- end namespace System.Security.Cryptography.X509Certificates -->
<!-- start namespace System.Text.RegularExpressions --> <div> 
<h2>Namespace System.Text.RegularExpressions</h2>
<!-- start type Regex --> <div>
<h3>Type Changed: System.Text.RegularExpressions.Regex</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">protected System.Collections.IDictionary CapNames { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected System.Collections.IDictionary Caps { get; set; }</span>
</pre>
</div>

</div> <!-- end type Regex -->

</div> <!-- end namespace System.Text.RegularExpressions -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/System.Core.html'>System.Core.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.IO.MemoryMappedFiles --> <div> 
<h2>Namespace System.IO.MemoryMappedFiles</h2>
<!-- start type MemoryMappedFile --> <div>
<h3>Type Changed: System.IO.MemoryMappedFiles.MemoryMappedFile</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MemoryMappedFile CreateFromFile (System.IO.FileStream fileStream, string mapName, long capacity, MemoryMappedFileAccess access, System.IO.HandleInheritability inheritability, bool leaveOpen);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MemoryMappedFile CreateNew (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability inheritability);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MemoryMappedFile CreateOrOpen (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability inheritability);</span>
</pre>
</div>

</div> <!-- end type MemoryMappedFile -->

</div> <!-- end namespace System.IO.MemoryMappedFiles -->
<!-- start namespace System.IO.Pipes --> <div> 
<h2>Namespace System.IO.Pipes</h2>
<!-- start type NamedPipeClientStream --> <div>
<h3>Type Changed: System.IO.Pipes.NamedPipeClientStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync (int timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync (System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task ConnectAsync (int timeout, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~NamedPipeClientStream ();</span>
</pre>
</div>

</div> <!-- end type NamedPipeClientStream -->
<!-- start type NamedPipeServerStream --> <div>
<h3>Type Changed: System.IO.Pipes.NamedPipeServerStream</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WaitForConnectionAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WaitForConnectionAsync (System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type NamedPipeServerStream -->
<!-- start type PipeStream --> <div>
<h3>Type Changed: System.IO.Pipes.PipeStream</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void WaitForPipeDrain ();</span>
</pre>
</div>

</div> <!-- end type PipeStream -->

</div> <!-- end namespace System.IO.Pipes -->
<!-- start namespace System.Linq --> <div> 
<h2>Namespace System.Linq</h2>
<!-- start type Enumerable --> <div>
<h3>Type Changed: System.Linq.Enumerable</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;TSource&gt; Append&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source, TSource element);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Collections.Generic.IEnumerable&lt;TSource&gt; Prepend&lt;TSource&gt; (System.Collections.Generic.IEnumerable&lt;TSource&gt; source, TSource element);</span>
</pre>
</div>

</div> <!-- end type Enumerable -->

</div> <!-- end namespace System.Linq -->
<!-- start namespace System.Linq.Expressions --> <div> 
<h2>Namespace System.Linq.Expressions</h2>
<!-- start type Expression`1 --> <div>
<h3>Type Changed: System.Linq.Expressions.Expression`1</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public TDelegate Compile (bool preferInterpretation);</span>
</pre>
</div>

</div> <!-- end type Expression`1 -->
<!-- start type LambdaExpression --> <div>
<h3>Type Changed: System.Linq.Expressions.LambdaExpression</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Delegate Compile (bool preferInterpretation);</span>
</pre>
</div>

</div> <!-- end type LambdaExpression -->

</div> <!-- end namespace System.Linq.Expressions -->
<!-- start namespace System.Security.Cryptography --> <div> 
<h2>Namespace System.Security.Cryptography</h2>
<!-- start type CngAlgorithm --> <div>
<h3>Type Changed: System.Security.Cryptography.CngAlgorithm</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDiffieHellman { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngAlgorithm ECDsa { get; }</span>
</pre>
</div>

</div> <!-- end type CngAlgorithm -->
<!-- start type CngKey --> <div>
<h3>Type Changed: System.Security.Cryptography.CngKey</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CngAlgorithm Algorithm { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngAlgorithmGroup AlgorithmGroup { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngExportPolicies ExportPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeNCryptKeyHandle Handle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsEphemeral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsMachineKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string KeyName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int KeySize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngKeyUsages KeyUsage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IntPtr ParentWindowHandle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngProvider Provider { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Microsoft.Win32.SafeHandles.SafeNCryptProviderHandle ProviderHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CngUIPolicy UIPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string UniqueName { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Create (CngAlgorithm algorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Create (CngAlgorithm algorithm, string keyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Create (CngAlgorithm algorithm, string keyName, CngKeyCreationParameters creationParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Delete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Exists (string keyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Exists (string keyName, CngProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Exists (string keyName, CngProvider provider, CngKeyOpenOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] Export (CngKeyBlobFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public CngProperty GetProperty (string name, CngPropertyOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool HasProperty (string name, CngPropertyOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Import (byte[] keyBlob, CngKeyBlobFormat format);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Import (byte[] keyBlob, CngKeyBlobFormat format, CngProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (string keyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (Microsoft.Win32.SafeHandles.SafeNCryptKeyHandle keyHandle, CngKeyHandleOpenOptions keyHandleOpenOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (string keyName, CngProvider provider);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CngKey Open (string keyName, CngProvider provider, CngKeyOpenOptions openOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetProperty (CngProperty property);</span>
</pre>
</div>

</div> <!-- end type CngKey -->
<!-- start type CngKeyBlobFormat --> <div>
<h3>Type Changed: System.Security.Cryptography.CngKeyBlobFormat</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat EccFullPrivateBlob { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CngKeyBlobFormat EccFullPublicBlob { get; }</span>
</pre>
</div>

</div> <!-- end type CngKeyBlobFormat -->
<!-- start type ECDsa --> <div>
<h3>Type Changed: System.Security.Cryptography.ECDsa</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static ECDsa Create (ECCurve curve);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ECDsa Create (ECParameters parameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ECParameters ExportExplicitParameters (bool includePrivateParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual ECParameters ExportParameters (bool includePrivateParameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GenerateKey (ECCurve curve);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ImportParameters (ECParameters parameters);</span>
</pre>
</div>

</div> <!-- end type ECDsa -->
<!-- start type ECDsaCng --> <div>
<h3>Type Changed: System.Security.Cryptography.ECDsaCng</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public ECDsaCng (int keySize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ECDsaCng (CngKey key);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ECDsaCng (ECCurve curve);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CngKey Key { get; }</span>
</pre>
</div>

</div> <!-- end type ECDsaCng -->
<!-- start type RSACng --> <div>
<h3>Type Changed: System.Security.Cryptography.RSACng</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public RSACng (int keySize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RSACng (CngKey key);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CngKey Key { get; }</span>
</pre>
</div>

</div> <!-- end type RSACng -->
<div> <!-- start type ECCurve -->
<h3>New Type System.Security.Cryptography.ECCurve</h3>
<pre class='added' data-is-non-breaking="">
public struct ECCurve {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public byte[] A;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] B;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Cofactor;</span>
	<span class='added added-field ' data-is-non-breaking="">public ECCurve.ECCurveType CurveType;</span>
	<span class='added added-field ' data-is-non-breaking="">public ECPoint G;</span>
	<span class='added added-field ' data-is-non-breaking="">public HashAlgorithmName? Hash;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Order;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Polynomial;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Prime;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Seed;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool IsCharacteristic2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsExplicit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsNamed { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsPrime { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Oid Oid { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static ECCurve CreateFromFriendlyName (string oidFriendlyName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ECCurve CreateFromOid (Oid curveOid);</span>
	<span class='added added-method ' data-is-non-breaking="">public static ECCurve CreateFromValue (string oidValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Validate ();</span>

	// inner types
	[Serializable]
	public enum ECCurveType {
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType Characteristic2;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType Implicit;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType Named;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType PrimeMontgomery;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType PrimeShortWeierstrass;</span>
		<span class='added added-field ' data-is-non-breaking="">public static const ECCurve.ECCurveType PrimeTwistedEdwards;</span>
	}
	public static class NamedCurves {
		// properties
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP160r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP160t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP192r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP192t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP224r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP224t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP256r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP256t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP320r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP320t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP384r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP384t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP512r1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve brainpoolP512t1 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve nistP256 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve nistP384 { get; }</span>
		<span class='added added-property ' data-is-non-breaking="">public static ECCurve nistP521 { get; }</span>
	}
}
</pre>
</div> <!-- end type ECCurve -->
<div> <!-- start type ECParameters -->
<h3>New Type System.Security.Cryptography.ECParameters</h3>
<pre class='added' data-is-non-breaking="">
public struct ECParameters {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ECCurve Curve;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] D;</span>
	<span class='added added-field ' data-is-non-breaking="">public ECPoint Q;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Validate ();</span>
}
</pre>
</div> <!-- end type ECParameters -->
<div> <!-- start type ECPoint -->
<h3>New Type System.Security.Cryptography.ECPoint</h3>
<pre class='added' data-is-non-breaking="">
public struct ECPoint {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public byte[] X;</span>
	<span class='added added-field ' data-is-non-breaking="">public byte[] Y;</span>
}
</pre>
</div> <!-- end type ECPoint -->
<div> <!-- start type IncrementalHash -->
<h3>New Type System.Security.Cryptography.IncrementalHash</h3>
<pre class='added' data-is-non-breaking="">
public sealed class IncrementalHash : System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HashAlgorithmName AlgorithmName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AppendData (byte[] data);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AppendData (byte[] data, int offset, int count);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IncrementalHash CreateHMAC (HashAlgorithmName hashAlgorithm, byte[] key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static IncrementalHash CreateHash (HashAlgorithmName hashAlgorithm);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">public byte[] GetHashAndReset ();</span>
}
</pre>
</div> <!-- end type IncrementalHash -->

</div> <!-- end namespace System.Security.Cryptography -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/System.Data.html'>System.Data.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace Microsoft.SqlServer.Server --> <div> 
<h2>Namespace Microsoft.SqlServer.Server</h2>
<!-- start type SqlDataRecord --> <div>
<h3>Type Changed: Microsoft.SqlServer.Server.SqlDataRecord</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SqlDataRecord ();</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlDataRecord (SqlMetaData[] metaData);</span>
</pre>
</div>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int FieldCount { get; }
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> object this [int ordinal] { get; }
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> object this [string name] { get; }
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> bool GetBoolean (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> byte GetByte (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> long GetBytes (int ordinal, long fieldOffset, byte[] buffer, int bufferOffset, int length)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> char GetChar (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> long GetChars (int ordinal, long fieldOffset, char[] buffer, int bufferOffset, int length)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Data.IDataReader GetData (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> string GetDataTypeName (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.DateTime GetDateTime (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Decimal GetDecimal (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> double GetDouble (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Type GetFieldType (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> float GetFloat (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> System.Guid GetGuid (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> short GetInt16 (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int GetInt32 (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> long GetInt64 (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> string GetName (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int GetOrdinal (string name)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> string GetString (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> object GetValue (int ordinal)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> int GetValues (object[] values)
</div><div data-is-non-breaking="">	public virtual <span class='removed removed-inline '>final</span> bool IsDBNull (int ordinal)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.DateTimeOffset GetDateTimeOffset (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlBinary GetSqlBinary (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlBoolean GetSqlBoolean (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlByte GetSqlByte (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlBytes GetSqlBytes (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlChars GetSqlChars (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlDateTime GetSqlDateTime (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlDecimal GetSqlDecimal (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlDouble GetSqlDouble (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Type GetSqlFieldType (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlGuid GetSqlGuid (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlInt16 GetSqlInt16 (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlInt32 GetSqlInt32 (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlInt64 GetSqlInt64 (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SqlMetaData GetSqlMetaData (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlMoney GetSqlMoney (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlSingle GetSqlSingle (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlString GetSqlString (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual object GetSqlValue (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int GetSqlValues (object[] values);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Data.SqlTypes.SqlXml GetSqlXml (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.TimeSpan GetTimeSpan (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBoolean (int ordinal, bool value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetByte (int ordinal, byte value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetBytes (int ordinal, long fieldOffset, byte[] buffer, int bufferOffset, int length);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetChar (int ordinal, char value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetChars (int ordinal, long fieldOffset, char[] buffer, int bufferOffset, int length);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDBNull (int ordinal);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDateTime (int ordinal, System.DateTime value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDateTimeOffset (int ordinal, System.DateTimeOffset value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDecimal (int ordinal, System.Decimal value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDouble (int ordinal, double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetFloat (int ordinal, float value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetGuid (int ordinal, System.Guid value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetInt16 (int ordinal, short value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetInt32 (int ordinal, int value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetInt64 (int ordinal, long value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlBinary (int ordinal, System.Data.SqlTypes.SqlBinary value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlBoolean (int ordinal, System.Data.SqlTypes.SqlBoolean value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlByte (int ordinal, System.Data.SqlTypes.SqlByte value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlBytes (int ordinal, System.Data.SqlTypes.SqlBytes value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlChars (int ordinal, System.Data.SqlTypes.SqlChars value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlDateTime (int ordinal, System.Data.SqlTypes.SqlDateTime value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlDecimal (int ordinal, System.Data.SqlTypes.SqlDecimal value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlDouble (int ordinal, System.Data.SqlTypes.SqlDouble value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlGuid (int ordinal, System.Data.SqlTypes.SqlGuid value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlInt16 (int ordinal, System.Data.SqlTypes.SqlInt16 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlInt32 (int ordinal, System.Data.SqlTypes.SqlInt32 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlInt64 (int ordinal, System.Data.SqlTypes.SqlInt64 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlMoney (int ordinal, System.Data.SqlTypes.SqlMoney value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlSingle (int ordinal, System.Data.SqlTypes.SqlSingle value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlString (int ordinal, System.Data.SqlTypes.SqlString value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSqlXml (int ordinal, System.Data.SqlTypes.SqlXml value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetString (int ordinal, string value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTimeSpan (int ordinal, System.TimeSpan value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (int ordinal, object value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int SetValues (object[] values);</span>
</pre>
</div>

</div> <!-- end type SqlDataRecord -->
<!-- start type SqlMetaData --> <div>
<h3>Type Changed: Microsoft.SqlServer.Server.SqlMetaData</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, long maxLength, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, byte precision, byte scale, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, long maxLength, long locale, System.Data.SqlTypes.SqlCompareOptions compareOptions, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, string database, string owningSchema, string objectName, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SqlMetaData (string name, System.Data.SqlDbType dbType, long maxLength, byte precision, byte scale, long localeId, System.Data.SqlTypes.SqlCompareOptions compareOptions, System.Type userDefinedType, bool useServerDefault, bool isUniqueKey, System.Data.SqlClient.SortOrder columnSortOrder, int sortOrdinal);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool IsUniqueKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Data.SqlClient.SortOrder SortOrder { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int SortOrdinal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool UseServerDefault { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Data.SqlTypes.SqlXml Adjust (System.Data.SqlTypes.SqlXml value);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.DateTimeOffset Adjust (System.DateTimeOffset value);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.TimeSpan Adjust (System.TimeSpan value);</span>
</pre>
</div>

</div> <!-- end type SqlMetaData -->

</div> <!-- end namespace Microsoft.SqlServer.Server -->
<!-- start namespace System.Data.SqlClient --> <div> 
<h2>Namespace System.Data.SqlClient</h2>
<!-- start type SqlBulkCopy --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlBulkCopy</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool EnableStreaming { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void WriteToServer (System.Data.Common.DbDataReader reader);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.Common.DbDataReader reader);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task WriteToServerAsync (System.Data.Common.DbDataReader reader, System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type SqlBulkCopy -->
<!-- start type SqlCommand --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlCommand</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync (System.Data.CommandBehavior behavior);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync (System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;SqlDataReader&gt; ExecuteReaderAsync (System.Data.CommandBehavior behavior, System.Threading.CancellationToken cancellationToken);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Xml.XmlReader&gt; ExecuteXmlReaderAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;System.Xml.XmlReader&gt; ExecuteXmlReaderAsync (System.Threading.CancellationToken cancellationToken);</span>
</pre>
</div>

</div> <!-- end type SqlCommand -->
<!-- start type SqlConnection --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlConnection</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Guid ClientConnectionId { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void ResetStatistics ();</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Collections.IDictionary RetrieveStatistics ();</span>
</pre>
</div>

</div> <!-- end type SqlConnection -->
<!-- start type SqlException --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlException</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Guid ClientConnectionId { get; }</span>
</pre>
</div>

</div> <!-- end type SqlException -->
<!-- start type SqlParameter --> <div>
<h3>Type Changed: System.Data.SqlClient.SqlParameter</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string TypeName { get; set; }</span>
</pre>
</div>

</div> <!-- end type SqlParameter -->

</div> <!-- end namespace System.Data.SqlClient -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/System.ServiceModel.html'>System.ServiceModel.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.ServiceModel --> <div> 
<h2>Namespace System.ServiceModel</h2>
<!-- start type EndpointAddressBuilder --> <div>
<h3>Type Changed: System.ServiceModel.EndpointAddressBuilder</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public EndpointIdentity Identity { get; set; }</span>
</pre>
</div>

</div> <!-- end type EndpointAddressBuilder -->
<!-- start type InstanceContext --> <div>
<h3>Type Changed: System.ServiceModel.InstanceContext</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>System.Object</span> <span class='added '>System.ServiceModel.Channels.CommunicationObject</span>
<p>Modified constructors:</p>
<pre>
<div data-is-non-breaking="">	public InstanceContext (object <span class='removed removed-inline '>dummy</span> <span class='added '>implementation</span>)
</div></pre>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICommunicationObject</span>
	<span class='added added-interface ' data-is-non-breaking="">System.ServiceModel.IExtensibleObject&lt;InstanceContext&gt;</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">protected override System.TimeSpan DefaultCloseTimeout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">protected override System.TimeSpan DefaultOpenTimeout { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Threading.SynchronizationContext SynchronizationContext { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public object GetServiceInstance (Channels.Message message);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnAbort ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override System.IAsyncResult OnBeginClose (System.TimeSpan timeout, System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override System.IAsyncResult OnBeginOpen (System.TimeSpan timeout, System.AsyncCallback callback, object state);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnClose (System.TimeSpan timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnClosed ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnEndClose (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnEndOpen (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnFaulted ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnOpen (System.TimeSpan timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnOpened ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void OnOpening ();</span>
</pre>
</div>

</div> <!-- end type InstanceContext -->
<!-- start type MessageSecurityOverTcp --> <div>
<h3>Type Changed: System.ServiceModel.MessageSecurityOverTcp</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MessageSecurityOverTcp ();</span>
</pre>
</div>

</div> <!-- end type MessageSecurityOverTcp -->
<!-- start type TcpTransportSecurity --> <div>
<h3>Type Changed: System.ServiceModel.TcpTransportSecurity</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.SslProtocols SslProtocols { get; set; }</span>
</pre>
</div>

</div> <!-- end type TcpTransportSecurity -->

</div> <!-- end namespace System.ServiceModel -->
<!-- start namespace System.ServiceModel.Channels --> <div> 
<h2>Namespace System.ServiceModel.Channels</h2>
<!-- start type SecurityBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.SecurityBindingElement</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.Tokens.SupportingTokenParameters EndpointSupportingTokenParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.MessageSecurityVersion MessageSecurityVersion { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public SecurityHeaderLayout SecurityHeaderLayout { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SecurityBindingElement CreateSecureConversationBindingElement (SecurityBindingElement binding);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecurityBindingElement CreateSecureConversationBindingElement (SecurityBindingElement binding, bool requireCancellation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SecurityBindingElement CreateSecureConversationBindingElement (SecurityBindingElement binding, bool requireCancellation, System.ServiceModel.Security.ChannelProtectionRequirements protectionRequirements);</span>
</pre>
</div>

</div> <!-- end type SecurityBindingElement -->
<!-- start type SslStreamSecurityBindingElement --> <div>
<h3>Type Changed: System.ServiceModel.Channels.SslStreamSecurityBindingElement</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.SslProtocols SslProtocols { get; set; }</span>
</pre>
</div>

</div> <!-- end type SslStreamSecurityBindingElement -->

</div> <!-- end namespace System.ServiceModel.Channels -->
<!-- start namespace System.ServiceModel.Description --> <div> 
<h2>Namespace System.ServiceModel.Description</h2>
<!-- start type ClientCredentials --> <div>
<h3>Type Changed: System.ServiceModel.Description.ClientCredentials</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.X509CertificateInitiatorClientCredential ClientCertificate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.HttpDigestClientCredential HttpDigest { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.X509CertificateRecipientClientCredential ServiceCertificate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.ServiceModel.Security.WindowsClientCredential Windows { get; }</span>
</pre>
</div>

</div> <!-- end type ClientCredentials -->

</div> <!-- end namespace System.ServiceModel.Description -->
<!-- start namespace System.ServiceModel.Security --> <div> 
<h2>Namespace System.ServiceModel.Security</h2>
<div> <!-- start type ChannelProtectionRequirements -->
<h3>New Type System.ServiceModel.Security.ChannelProtectionRequirements</h3>
<pre class='added' data-is-non-breaking="">
public class ChannelProtectionRequirements {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ChannelProtectionRequirements ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ChannelProtectionRequirements (ChannelProtectionRequirements other);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification IncomingEncryptionParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification IncomingSignatureParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification OutgoingEncryptionParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ScopedMessagePartSpecification OutgoingSignatureParts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Add (ChannelProtectionRequirements protectionRequirements);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Add (ChannelProtectionRequirements protectionRequirements, bool channelScopeOnly);</span>
	<span class='added added-method ' data-is-non-breaking="">public ChannelProtectionRequirements CreateInverse ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void MakeReadOnly ();</span>
}
</pre>
</div> <!-- end type ChannelProtectionRequirements -->
<div> <!-- start type MessagePartSpecification -->
<h3>New Type System.ServiceModel.Security.MessagePartSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class MessagePartSpecification {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification (bool isBodyIncluded);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification (System.Xml.XmlQualifiedName[] headerTypes);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MessagePartSpecification (bool isBodyIncluded, System.Xml.XmlQualifiedName[] headerTypes);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.ICollection&lt;System.Xml.XmlQualifiedName&gt; HeaderTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsBodyIncluded { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsReadOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static MessagePartSpecification NoParts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Clear ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void MakeReadOnly ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void Union (MessagePartSpecification other);</span>
}
</pre>
</div> <!-- end type MessagePartSpecification -->
<div> <!-- start type ScopedMessagePartSpecification -->
<h3>New Type System.ServiceModel.Security.ScopedMessagePartSpecification</h3>
<pre class='added' data-is-non-breaking="">
public class ScopedMessagePartSpecification {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public ScopedMessagePartSpecification ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public ScopedMessagePartSpecification (ScopedMessagePartSpecification other);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.ICollection&lt;string&gt; Actions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MessagePartSpecification ChannelParts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IsReadOnly { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void AddParts (MessagePartSpecification parts);</span>
	<span class='added added-method ' data-is-non-breaking="">public void AddParts (MessagePartSpecification parts, string action);</span>
	<span class='added added-method ' data-is-non-breaking="">public void MakeReadOnly ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool TryGetParts (string action, out MessagePartSpecification parts);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool TryGetParts (string action, bool excludeChannelScope, out MessagePartSpecification parts);</span>
}
</pre>
</div> <!-- end type ScopedMessagePartSpecification -->
<div> <!-- start type X509CertificateInitiatorClientCredential -->
<h3>New Type System.ServiceModel.Security.X509CertificateInitiatorClientCredential</h3>
<pre class='added' data-is-non-breaking="">
public sealed class X509CertificateInitiatorClientCredential {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509Certificate2 Certificate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void SetCertificate (string subjectName, System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetCertificate (System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Security.Cryptography.X509Certificates.X509FindType findType, object findValue);</span>
}
</pre>
</div> <!-- end type X509CertificateInitiatorClientCredential -->
<div> <!-- start type X509CertificateRecipientClientCredential -->
<h3>New Type System.ServiceModel.Security.X509CertificateRecipientClientCredential</h3>
<pre class='added' data-is-non-breaking="">
public sealed class X509CertificateRecipientClientCredential {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public X509ServiceCertificateAuthentication Authentication { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509Certificate2 DefaultCertificate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.Dictionary&lt;System.Uri,System.Security.Cryptography.X509Certificates.X509Certificate2&gt; ScopedCertificates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public X509ServiceCertificateAuthentication SslCertificateAuthentication { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void SetDefaultCertificate (string subjectName, System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetDefaultCertificate (System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Security.Cryptography.X509Certificates.X509FindType findType, object findValue);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetScopedCertificate (string subjectName, System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Uri targetService);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetScopedCertificate (System.Security.Cryptography.X509Certificates.StoreLocation storeLocation, System.Security.Cryptography.X509Certificates.StoreName storeName, System.Security.Cryptography.X509Certificates.X509FindType findType, object findValue, System.Uri targetService);</span>
}
</pre>
</div> <!-- end type X509CertificateRecipientClientCredential -->
<div> <!-- start type X509ServiceCertificateAuthentication -->
<h3>New Type System.ServiceModel.Security.X509ServiceCertificateAuthentication</h3>
<pre class='added' data-is-non-breaking="">
public class X509ServiceCertificateAuthentication {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public X509ServiceCertificateAuthentication ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public X509CertificateValidationMode CertificateValidationMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.IdentityModel.Selectors.X509CertificateValidator CustomCertificateValidator { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509RevocationMode RevocationMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.StoreLocation TrustedStoreLocation { get; set; }</span>
}
</pre>
</div> <!-- end type X509ServiceCertificateAuthentication -->

</div> <!-- end namespace System.ServiceModel.Security -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/System.Transactions.html'>System.Transactions.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Transactions --> <div> 
<h2>Namespace System.Transactions</h2>
<!-- start type TransactionScope --> <div>
<h3>Type Changed: System.Transactions.TransactionScope</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public TransactionScope (TransactionScopeAsyncFlowOption asyncFlow);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TransactionScope (TransactionScopeOption option, TransactionScopeAsyncFlowOption asyncFlow);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public TransactionScope (TransactionScopeOption option, System.TimeSpan timeout, TransactionScopeAsyncFlowOption asyncFlow);</span>
</pre>
</div>

</div> <!-- end type TransactionScope -->
<div> <!-- start type TransactionScopeAsyncFlowOption -->
<h3>New Type System.Transactions.TransactionScopeAsyncFlowOption</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum TransactionScopeAsyncFlowOption {
	<span class='added added-field ' data-is-non-breaking="">Enabled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Suppress = 0,</span>
}
</pre>
</div> <!-- end type TransactionScopeAsyncFlowOption -->

</div> <!-- end namespace System.Transactions -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/Xamarin.TVOS.html'>Xamarin.TVOS.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAssetDownloadDelegate --> <div>
<h3>Type Changed: AVFoundation.AVAssetDownloadDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishCollectingMetrics (Foundation.NSUrlSession session, Foundation.NSUrlSessionTask task, Foundation.NSUrlSessionTaskMetrics metrics);</span>
</pre>
</div>

</div> <!-- end type AVAssetDownloadDelegate -->
<!-- start type AVAudioChannelLayout --> <div>
<h3>Type Changed: AVFoundation.AVAudioChannelLayout</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Valid instance of this type cannot be directly created")]
	public AVAudioChannelLayout ();</span>
</div></pre>

</div> <!-- end type AVAudioChannelLayout -->
<!-- start type AVAudioConnectionPoint --> <div>
<h3>Type Changed: AVFoundation.AVAudioConnectionPoint</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Valid instance of this type cannot be directly created")]
	public AVAudioConnectionPoint ();</span>
</div></pre>

</div> <!-- end type AVAudioConnectionPoint -->
<!-- start type AVAudioConverterPrimeInfo --> <div>
<h3>Type Changed: AVFoundation.AVAudioConverterPrimeInfo</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioConverterPrimeInfo (uint leadingFrames, uint trailingFrames);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVAudioConverterPrimeInfo other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVAudioConverterPrimeInfo left, AVAudioConverterPrimeInfo right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVAudioConverterPrimeInfo left, AVAudioConverterPrimeInfo right);</span>
</pre>
</div>

</div> <!-- end type AVAudioConverterPrimeInfo -->
<!-- start type AVAudioSessionCategoryOptions --> <div>
<h3>Type Changed: AVFoundation.AVAudioSessionCategoryOptions</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AllowAirPlay = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">AllowBluetoothA2DP = 32,</span>
</pre>
</div>

</div> <!-- end type AVAudioSessionCategoryOptions -->
<!-- start type AVBeatRange --> <div>
<h3>Type Changed: AVFoundation.AVBeatRange</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVBeatRange other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVBeatRange left, AVBeatRange right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVBeatRange left, AVBeatRange right);</span>
</pre>
</div>

</div> <!-- end type AVBeatRange -->
<!-- start type AVCaptureWhiteBalanceChromaticityValues --> <div>
<h3>Type Changed: AVFoundation.AVCaptureWhiteBalanceChromaticityValues</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVCaptureWhiteBalanceChromaticityValues other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVCaptureWhiteBalanceChromaticityValues left, AVCaptureWhiteBalanceChromaticityValues right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVCaptureWhiteBalanceChromaticityValues left, AVCaptureWhiteBalanceChromaticityValues right);</span>
</pre>
</div>

</div> <!-- end type AVCaptureWhiteBalanceChromaticityValues -->
<!-- start type AVCaptureWhiteBalanceGains --> <div>
<h3>Type Changed: AVFoundation.AVCaptureWhiteBalanceGains</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVCaptureWhiteBalanceGains other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVCaptureWhiteBalanceGains left, AVCaptureWhiteBalanceGains right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVCaptureWhiteBalanceGains left, AVCaptureWhiteBalanceGains right);</span>
</pre>
</div>

</div> <!-- end type AVCaptureWhiteBalanceGains -->
<!-- start type AVCaptureWhiteBalanceTemperatureAndTintValues --> <div>
<h3>Type Changed: AVFoundation.AVCaptureWhiteBalanceTemperatureAndTintValues</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public bool Equals (AVCaptureWhiteBalanceTemperatureAndTintValues other);</span>
	<span class='added added-method ' data-is-non-breaking="">public override bool Equals (object obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public override int GetHashCode ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (AVCaptureWhiteBalanceTemperatureAndTintValues left, AVCaptureWhiteBalanceTemperatureAndTintValues right);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (AVCaptureWhiteBalanceTemperatureAndTintValues left, AVCaptureWhiteBalanceTemperatureAndTintValues right);</span>
</pre>
</div>

</div> <!-- end type AVCaptureWhiteBalanceTemperatureAndTintValues -->
<!-- start type AVError --> <div>
<h3>Type Changed: AVFoundation.AVError</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	ApplicationIsNotAuthorizedToUseDevice = <span class='removed removed-inline removed-breaking-inline'>11852</span> <span class='added '>-11852</span>
</div><div data-is-breaking="">	MaximumStillImageCaptureRequestsExceeded = <span class='removed removed-inline removed-breaking-inline'>11830</span> <span class='added '>-11830</span>
</div></pre>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">OperationNotAllowed = -11862,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedOutputSettings = -11861,</span>
</pre>
</div>

</div> <!-- end type AVError -->
<div> <!-- start type AVMusicTrackLoopCount -->
<h3>New Type AVFoundation.AVMusicTrackLoopCount</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVMusicTrackLoopCount {
	<span class='added added-field ' data-is-non-breaking="">Forever = -1,</span>
}
</pre>
</div> <!-- end type AVMusicTrackLoopCount -->
<div> <!-- start type AVPlayerTimeControlStatus -->
<h3>New Type AVFoundation.AVPlayerTimeControlStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AVPlayerTimeControlStatus {
	<span class='added added-field ' data-is-non-breaking="">Paused = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Playing = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">WaitingToPlayAtSpecifiedRate = 1,</span>
}
</pre>
</div> <!-- end type AVPlayerTimeControlStatus -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AudioToolbox --> <div> 
<h2>Namespace AudioToolbox</h2>
<!-- start type MusicSequence --> <div>
<h3>Type Changed: AudioToolbox.MusicSequence</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public MusicTrack GetTempoTrack ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetUserCallback (MusicSequenceUserCallback callback);</span>
</pre>
</div>

</div> <!-- end type MusicSequence -->
<div> <!-- start type MusicSequenceUserCallback -->
<h3>New Type AudioToolbox.MusicSequenceUserCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MusicSequenceUserCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MusicSequenceUserCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (MusicTrack track, double inEventTime, MusicEventUserData inEventData, double inStartSliceBeat, double inEndSliceBeat, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (MusicTrack track, double inEventTime, MusicEventUserData inEventData, double inStartSliceBeat, double inEndSliceBeat);</span>
}
</pre>
</div> <!-- end type MusicSequenceUserCallback -->

</div> <!-- end namespace AudioToolbox -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUHostTransportStateBlock TransportStateBlock { get; set; }</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->
<!-- start type AUAudioUnit_AUAudioInputOutputUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit_AUAudioInputOutputUnit</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static AUInputHandler GetInputHandler (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static AURenderPullInputBlock GetOutputProvider (AUAudioUnit This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetInputHandler (AUAudioUnit This, AUInputHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetOutputProvider (AUAudioUnit This, AURenderPullInputBlock provider);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit_AUAudioInputOutputUnit -->
<!-- start type AUParameter --> <div>
<h3>Type Changed: AudioUnit.AUParameter</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void SetValue (float value, IntPtr originator);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void SetValue (float value, IntPtr originator, ulong hostTime);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (float value, AUParameterObserverToken originator);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetValue (float value, AUParameterObserverToken originator, ulong hostTime);</span>
</pre>
</div>

</div> <!-- end type AUParameter -->
<!-- start type AUParameterNode --> <div>
<h3>Type Changed: AudioUnit.AUParameterNode</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> AUImplementorStringFromValueCallback ImplementorStringFromValueCallback { get; set; }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUImplementorDisplayNameWithLengthCallback ImplementorDisplayNameWithLengthCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AUImplementorValueFromStringCallback ImplementorValueFromStringCallback { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the AUParameterObserverToken overload")]
	public virtual void RemoveParameterObserver (IntPtr token);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the CreateTokenByAddingParameterObserver instead")]
	public virtual IntPtr TokenByAddingParameterObserver (AUParameterObserver observer);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterObserver (AUParameterObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public AUParameterObserverToken CreateTokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public void RemoveParameterObserver (AUParameterObserverToken token);</span>

	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use the CreateTokenByAddingParameterRecordingObserver instead")]
	public virtual IntPtr TokenByAddingParameterRecordingObserver (AUParameterRecordingObserver observer);</span>
</pre>
</div>

</div> <!-- end type AUParameterNode -->
<div> <!-- start type AUHostTransportStateBlock -->
<h3>New Type AudioUnit.AUHostTransportStateBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUHostTransportStateBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUHostTransportStateBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool EndInvoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Invoke (ref AUHostTransportStateFlags transportStateFlags, ref double currentSamplePosition, ref double cycleStartBeatPosition, ref double cycleEndBeatPosition);</span>
}
</pre>
</div> <!-- end type AUHostTransportStateBlock -->
<div> <!-- start type AUImplementorDisplayNameWithLengthCallback -->
<h3>New Type AudioUnit.AUImplementorDisplayNameWithLengthCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUImplementorDisplayNameWithLengthCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUImplementorDisplayNameWithLengthCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AUParameterNode node, nint desiredLength, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string Invoke (AUParameterNode node, nint desiredLength);</span>
}
</pre>
</div> <!-- end type AUImplementorDisplayNameWithLengthCallback -->
<div> <!-- start type AUImplementorValueFromStringCallback -->
<h3>New Type AudioUnit.AUImplementorValueFromStringCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUImplementorValueFromStringCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUImplementorValueFromStringCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AUParameter param, string str, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual float Invoke (AUParameter param, string str);</span>
}
</pre>
</div> <!-- end type AUImplementorValueFromStringCallback -->
<div> <!-- start type AUInputHandler -->
<h3>New Type AudioUnit.AUInputHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUInputHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUInputHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (ref AudioUnitRenderActionFlags actionFlags, ref AudioToolbox.AudioTimeStamp timestamp, uint frameCount, nint inputBusNumber, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref AudioUnitRenderActionFlags actionFlags, ref AudioToolbox.AudioTimeStamp timestamp, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (ref AudioUnitRenderActionFlags actionFlags, ref AudioToolbox.AudioTimeStamp timestamp, uint frameCount, nint inputBusNumber);</span>
}
</pre>
</div> <!-- end type AUInputHandler -->
<div> <!-- start type AUParameterObserverToken -->
<h3>New Type AudioUnit.AUParameterObserverToken</h3>
<pre class='added' data-is-non-breaking="">
public struct AUParameterObserverToken {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public IntPtr ObserverToken;</span>
}
</pre>
</div> <!-- end type AUParameterObserverToken -->
<div> <!-- start type AUParameterRecordingObserver -->
<h3>New Type AudioUnit.AUParameterRecordingObserver</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AUParameterRecordingObserver : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AUParameterRecordingObserver (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (nint numberOfEvents, ref AURecordedParameterEvent events, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref AURecordedParameterEvent events, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (nint numberOfEvents, ref AURecordedParameterEvent events);</span>
}
</pre>
</div> <!-- end type AUParameterRecordingObserver -->
<div> <!-- start type AURecordedParameterEvent -->
<h3>New Type AudioUnit.AURecordedParameterEvent</h3>
<pre class='added' data-is-non-breaking="">
public struct AURecordedParameterEvent {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public ulong Address;</span>
	<span class='added added-field ' data-is-non-breaking="">public ulong HostTime;</span>
	<span class='added added-field ' data-is-non-breaking="">public float Value;</span>
}
</pre>
</div> <!-- end type AURecordedParameterEvent -->
<div> <!-- start type IAUAudioUnitFactory -->
<h3>New Type AudioUnit.IAUAudioUnitFactory</h3>
<pre class='added' data-is-non-breaking="">
public interface IAUAudioUnitFactory : Foundation.INSExtensionRequestHandling, ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual AUAudioUnit CreateAudioUnit (AudioComponentDescription desc, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type IAUAudioUnitFactory -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace CloudKit --> <div> 
<h2>Namespace CloudKit</h2>
<!-- start type CKContainer --> <div>
<h3>Type Changed: CloudKit.CKContainer</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CurrentUserDefaultName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabase SharedCloudDatabase { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AcceptShareMetadata (CKShareMetadata metadata, System.Action&lt;CKShare,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShare&gt; AcceptShareMetadataAsync (CKShareMetadata metadata);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverUserIdentity (CKRecordID userRecordID, System.Action&lt;CKUserIdentity,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKUserIdentity&gt; DiscoverUserIdentityAsync (CKRecordID userRecordID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverUserIdentityWithEmailAddress (string email, System.Action&lt;CKUserIdentity,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKUserIdentity&gt; DiscoverUserIdentityWithEmailAddressAsync (string email);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscoverUserIdentityWithPhoneNumber (string phoneNumber, System.Action&lt;CKUserIdentity,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKUserIdentity&gt; DiscoverUserIdentityWithPhoneNumberAsync (string phoneNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareMetadata (Foundation.NSUrl url, System.Action&lt;CKShareMetadata,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareMetadata&gt; FetchShareMetadataAsync (Foundation.NSUrl url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareParticipant (CKRecordID userRecordID, System.Action&lt;CKShareParticipant,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareParticipant&gt; FetchShareParticipantAsync (CKRecordID userRecordID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareParticipantWithEmailAddress (string emailAddress, System.Action&lt;CKShareParticipant,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareParticipant&gt; FetchShareParticipantWithEmailAddressAsync (string emailAddress);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FetchShareParticipantWithPhoneNumber (string phoneNumber, System.Action&lt;CKShareParticipant,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;CKShareParticipant&gt; FetchShareParticipantWithPhoneNumberAsync (string phoneNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CKDatabase GetDatabase (CKDatabaseScope databaseScope);</span>
</pre>
</div>

</div> <!-- end type CKContainer -->
<!-- start type CKDatabase --> <div>
<h3>Type Changed: CloudKit.CKDatabase</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
</pre>
</div>

</div> <!-- end type CKDatabase -->
<!-- start type CKErrorCode --> <div>
<h3>Type Changed: CloudKit.CKErrorCode</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AlreadyShared = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedAccountRestricted = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">ParticipantMayNeedVerification = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">ReferenceViolation = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">TooManyParticipants = 29,</span>
</pre>
</div>

</div> <!-- end type CKErrorCode -->
<!-- start type CKFetchNotificationChangesOperation --> <div>
<h3>Type Changed: CloudKit.CKFetchNotificationChangesOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKFetchNotificationChangesOperation ();</span>
</pre>

</div> <!-- end type CKFetchNotificationChangesOperation -->
<!-- start type CKFetchRecordZonesOperation --> <div>
<h3>Type Changed: CloudKit.CKFetchRecordZonesOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKFetchRecordZonesOperation ();</span>
</pre>

</div> <!-- end type CKFetchRecordZonesOperation -->
<!-- start type CKFetchRecordsOperation --> <div>
<h3>Type Changed: CloudKit.CKFetchRecordsOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKFetchRecordsOperation ();</span>
</pre>

</div> <!-- end type CKFetchRecordsOperation -->
<!-- start type CKFetchWebAuthTokenOperation --> <div>
<h3>Type Changed: CloudKit.CKFetchWebAuthTokenOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKFetchWebAuthTokenOperation ();</span>
</pre>

</div> <!-- end type CKFetchWebAuthTokenOperation -->
<!-- start type CKLocationSortDescriptor --> <div>
<h3>Type Changed: CloudKit.CKLocationSortDescriptor</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKLocationSortDescriptor ();</span>
</pre>

</div> <!-- end type CKLocationSortDescriptor -->
<!-- start type CKModifyBadgeOperation --> <div>
<h3>Type Changed: CloudKit.CKModifyBadgeOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKModifyBadgeOperation ();</span>
</pre>

</div> <!-- end type CKModifyBadgeOperation -->
<!-- start type CKModifyRecordZonesOperation --> <div>
<h3>Type Changed: CloudKit.CKModifyRecordZonesOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKModifyRecordZonesOperation ();</span>
</pre>

</div> <!-- end type CKModifyRecordZonesOperation -->
<!-- start type CKModifyRecordsOperation --> <div>
<h3>Type Changed: CloudKit.CKModifyRecordsOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKModifyRecordsOperation ();</span>
</pre>

</div> <!-- end type CKModifyRecordsOperation -->
<!-- start type CKNotification --> <div>
<h3>Type Changed: CloudKit.CKNotification</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Badge { get; }</span>
</pre>
</div>

</div> <!-- end type CKNotification -->
<!-- start type CKNotificationID --> <div>
<h3>Type Changed: CloudKit.CKNotificationID</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKNotificationID ();</span>
</pre>

</div> <!-- end type CKNotificationID -->
<!-- start type CKNotificationInfo --> <div>
<h3>Type Changed: CloudKit.CKNotificationInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldBadge { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldSendContentAvailable { get; set; }</span>
</pre>
</div>

</div> <!-- end type CKNotificationInfo -->
<!-- start type CKNotificationType --> <div>
<h3>Type Changed: CloudKit.CKNotificationType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Database = 4,</span>
</pre>
</div>

</div> <!-- end type CKNotificationType -->
<!-- start type CKOperation --> <div>
<h3>Type Changed: CloudKit.CKOperation</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeoutIntervalForRequest { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeoutIntervalForResource { get; set; }</span>
</pre>
</div>

</div> <!-- end type CKOperation -->
<!-- start type CKQueryNotification --> <div>
<h3>Type Changed: CloudKit.CKQueryNotification</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
</pre>
</div>

</div> <!-- end type CKQueryNotification -->
<!-- start type CKQueryOperation --> <div>
<h3>Type Changed: CloudKit.CKQueryOperation</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKQueryOperation ();</span>
</pre>

</div> <!-- end type CKQueryOperation -->
<!-- start type CKRecord --> <div>
<h3>Type Changed: CloudKit.CKRecord</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKReference Parent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RecordParentKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString RecordShareKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKReference Share { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TypeShare { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetParent (CKRecord parentRecord);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetParent (CKRecordID parentRecordID);</span>
</pre>
</div>

</div> <!-- end type CKRecord -->
<!-- start type CKRecordZone --> <div>
<h3>Type Changed: CloudKit.CKRecordZone</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CKRecordZone ();</span>
</pre>

</div> <!-- end type CKRecordZone -->
<!-- start type CKRecordZoneCapabilities --> <div>
<h3>Type Changed: CloudKit.CKRecordZoneCapabilities</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Sharing = 4,</span>
</pre>
</div>

</div> <!-- end type CKRecordZoneCapabilities -->
<!-- start type CKRecordZoneNotification --> <div>
<h3>Type Changed: CloudKit.CKRecordZoneNotification</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
</pre>
</div>

</div> <!-- end type CKRecordZoneNotification -->
<!-- start type CKSubscriptionType --> <div>
<h3>Type Changed: CloudKit.CKSubscriptionType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Database = 3,</span>
</pre>
</div>

</div> <!-- end type CKSubscriptionType -->
<div> <!-- start type CKAcceptPerShareCompletionHandler -->
<h3>New Type CloudKit.CKAcceptPerShareCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKAcceptPerShareCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKAcceptPerShareCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKShareMetadata shareMetadata, CKShare acceptedShare, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKShareMetadata shareMetadata, CKShare acceptedShare, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CKAcceptPerShareCompletionHandler -->
<div> <!-- start type CKAcceptSharesOperation -->
<h3>New Type CloudKit.CKAcceptSharesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKAcceptSharesOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKAcceptSharesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKAcceptSharesOperation (CKShareMetadata[] shareMetadatas);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKAcceptSharesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKAcceptSharesOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; AcceptSharesCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKAcceptPerShareCompletionHandler PerShareCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareMetadata[] ShareMetadatas { get; set; }</span>
}
</pre>
</div> <!-- end type CKAcceptSharesOperation -->
<div> <!-- start type CKDatabaseNotification -->
<h3>New Type CloudKit.CKDatabaseNotification</h3>
<pre class='added' data-is-non-breaking="">
public class CKDatabaseNotification : CloudKit.CKNotification, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKDatabaseNotification (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseNotification (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseNotification (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKDatabaseScope DatabaseScope { get; }</span>
}
</pre>
</div> <!-- end type CKDatabaseNotification -->
<div> <!-- start type CKDatabaseScope -->
<h3>New Type CloudKit.CKDatabaseScope</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKDatabaseScope {
	<span class='added added-field ' data-is-non-breaking="">Private = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Public = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Shared = 3,</span>
}
</pre>
</div> <!-- end type CKDatabaseScope -->
<div> <!-- start type CKDatabaseSubscription -->
<h3>New Type CloudKit.CKDatabaseSubscription</h3>
<pre class='added' data-is-non-breaking="">
public class CKDatabaseSubscription : CloudKit.CKSubscription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKDatabaseSubscription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseSubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDatabaseSubscription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKDatabaseSubscription (string subscriptionID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RecordType { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKDatabaseSubscription -->
<div> <!-- start type CKDiscoverUserIdentitiesOperation -->
<h3>New Type CloudKit.CKDiscoverUserIdentitiesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKDiscoverUserIdentitiesOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKDiscoverUserIdentitiesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKDiscoverUserIdentitiesOperation (CKUserIdentityLookupInfo[] userIdentityLookupInfos);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDiscoverUserIdentitiesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKDiscoverUserIdentitiesOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; Completed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKUserIdentity,CloudKit.CKUserIdentityLookupInfo&gt; Discovered { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentityLookupInfo[] UserIdentityLookupInfos { get; set; }</span>
}
</pre>
</div> <!-- end type CKDiscoverUserIdentitiesOperation -->
<div> <!-- start type CKFetchDatabaseChangesCompletionHandler -->
<h3>New Type CloudKit.CKFetchDatabaseChangesCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchDatabaseChangesCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchDatabaseChangesCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKServerChangeToken serverChangeToken, bool moreComing, Foundation.NSError operationError, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKServerChangeToken serverChangeToken, bool moreComing, Foundation.NSError operationError);</span>
}
</pre>
</div> <!-- end type CKFetchDatabaseChangesCompletionHandler -->
<div> <!-- start type CKFetchDatabaseChangesOperation -->
<h3>New Type CloudKit.CKFetchDatabaseChangesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchDatabaseChangesOperation : CloudKit.CKDatabaseOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchDatabaseChangesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchDatabaseChangesOperation (CKServerChangeToken previousServerChangeToken);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchDatabaseChangesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchDatabaseChangesOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKServerChangeToken&gt; ChangeTokenUpdated { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKRecordZoneID&gt; Changed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchDatabaseChangesCompletionHandler ChangesCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FetchAllChanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ResultsLimit { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKRecordZoneID&gt; WasDeleted { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchDatabaseChangesOperation -->
<div> <!-- start type CKFetchPerShareMetadataHandler -->
<h3>New Type CloudKit.CKFetchPerShareMetadataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchPerShareMetadataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchPerShareMetadataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSUrl shareURL, CKShareMetadata shareMetadata, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSUrl shareURL, CKShareMetadata shareMetadata, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CKFetchPerShareMetadataHandler -->
<div> <!-- start type CKFetchRecordZoneChangesFetchCompletedHandler -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesFetchCompletedHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchRecordZoneChangesFetchCompletedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesFetchCompletedHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, bool moreComing, Foundation.NSError recordZoneError, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, bool moreComing, Foundation.NSError recordZoneError);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesFetchCompletedHandler -->
<div> <!-- start type CKFetchRecordZoneChangesOperation -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchRecordZoneChangesOperation : CloudKit.CKDatabaseOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOperation (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOperation (CKRecordZoneID[] recordZoneIDs, Foundation.NSDictionary&lt;CKRecordZoneID,CloudKit.CKFetchRecordZoneChangesOptions&gt; optionsByRecordZoneID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; ChangesCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FetchAllChanges { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchRecordZoneChangesFetchCompletedHandler FetchCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;CKRecordZoneID,CloudKit.CKFetchRecordZoneChangesOptions&gt; OptionsByRecordZoneID { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKRecord&gt; RecordChanged { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchRecordZoneChangesWithIDWasDeletedHandler RecordWithIDWasDeleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchRecordZoneChangesTokensUpdatedHandler RecordZoneChangeTokensUpdated { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordZoneID[] RecordZoneIDs { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesOperation -->
<div> <!-- start type CKFetchRecordZoneChangesOptions -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchRecordZoneChangesOptions : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesOptions (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchRecordZoneChangesOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] DesiredKeys { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ResultsLimit { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesOptions -->
<div> <!-- start type CKFetchRecordZoneChangesTokensUpdatedHandler -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesTokensUpdatedHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchRecordZoneChangesTokensUpdatedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesTokensUpdatedHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKRecordZoneID recordZoneID, CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesTokensUpdatedHandler -->
<div> <!-- start type CKFetchRecordZoneChangesWithIDWasDeletedHandler -->
<h3>New Type CloudKit.CKFetchRecordZoneChangesWithIDWasDeletedHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate CKFetchRecordZoneChangesWithIDWasDeletedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchRecordZoneChangesWithIDWasDeletedHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (CKRecordID recordID, Foundation.NSString recordType, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (CKRecordID recordID, Foundation.NSString recordType);</span>
}
</pre>
</div> <!-- end type CKFetchRecordZoneChangesWithIDWasDeletedHandler -->
<div> <!-- start type CKFetchShareMetadataOperation -->
<h3>New Type CloudKit.CKFetchShareMetadataOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchShareMetadataOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareMetadataOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareMetadataOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareMetadataOperation (Foundation.NSUrl[] shareUrls);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareMetadataOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; FetchShareMetadataCompleted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKFetchPerShareMetadataHandler PerShareMetadata { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] RootRecordDesiredKeys { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl[] ShareUrls { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldFetchRootRecord { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchShareMetadataOperation -->
<div> <!-- start type CKFetchShareParticipantsOperation -->
<h3>New Type CloudKit.CKFetchShareParticipantsOperation</h3>
<pre class='added' data-is-non-breaking="">
public class CKFetchShareParticipantsOperation : CloudKit.CKOperation, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareParticipantsOperation ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKFetchShareParticipantsOperation (CKUserIdentityLookupInfo[] userIdentityLookupInfos);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareParticipantsOperation (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKFetchShareParticipantsOperation (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;Foundation.NSError&gt; Completed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;CKShareParticipant&gt; Fetched { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentityLookupInfo[] UserIdentityLookupInfos { get; set; }</span>
}
</pre>
</div> <!-- end type CKFetchShareParticipantsOperation -->
<div> <!-- start type CKQuerySubscription -->
<h3>New Type CloudKit.CKQuerySubscription</h3>
<pre class='added' data-is-non-breaking="">
public class CKQuerySubscription : CloudKit.CKSubscription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKQuerySubscription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKQuerySubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKQuerySubscription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKQuerySubscription (string recordType, Foundation.NSPredicate predicate, CKQuerySubscriptionOptions querySubscriptionOptions);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKQuerySubscription (string recordType, Foundation.NSPredicate predicate, string subscriptionID, CKQuerySubscriptionOptions querySubscriptionOptions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RecordType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKQuerySubscriptionOptions SubscriptionOptions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordZoneID ZoneID { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKQuerySubscription -->
<div> <!-- start type CKQuerySubscriptionOptions -->
<h3>New Type CloudKit.CKQuerySubscriptionOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKQuerySubscriptionOptions {
	<span class='added added-field ' data-is-non-breaking="">FiresOnce = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordCreation = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordDeletion = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">RecordUpdate = 2,</span>
}
</pre>
</div> <!-- end type CKQuerySubscriptionOptions -->
<div> <!-- start type CKRecordZoneSubscription -->
<h3>New Type CloudKit.CKRecordZoneSubscription</h3>
<pre class='added' data-is-non-breaking="">
public class CKRecordZoneSubscription : CloudKit.CKSubscription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKRecordZoneSubscription (CKRecordZoneID zoneID);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKRecordZoneSubscription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKRecordZoneSubscription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKRecordZoneSubscription (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKRecordZoneSubscription (CKRecordZoneID zoneID, string subscriptionID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RecordType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordZoneID ZoneID { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKRecordZoneSubscription -->
<div> <!-- start type CKShare -->
<h3>New Type CloudKit.CKShare</h3>
<pre class='added' data-is-non-breaking="">
public class CKShare : CloudKit.CKRecord, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKShare (CKRecord rootRecord);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKShare (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShare (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShare (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKShare (CKRecord rootRecord, CKRecordID shareID);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipant CurrentUser { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipant Owner { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipant[] Participants { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantPermission PublicPermission { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Add (CKShareParticipant participant);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Remove (CKShareParticipant participant);</span>
}
</pre>
</div> <!-- end type CKShare -->
<div> <!-- start type CKShareKeys -->
<h3>New Type CloudKit.CKShareKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class CKShareKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ThumbnailImageData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Title { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Type { get; }</span>
}
</pre>
</div> <!-- end type CKShareKeys -->
<div> <!-- start type CKShareMetadata -->
<h3>New Type CloudKit.CKShareMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class CKShareMetadata : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKShareMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKShareMetadata (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareMetadata (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareMetadata (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ContainerIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentity OwnerIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantPermission Permission { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecord RootRecord { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordID RootRecordID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShare Share { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantAcceptanceStatus Status { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKShareMetadata -->
<div> <!-- start type CKShareParticipant -->
<h3>New Type CloudKit.CKShareParticipant</h3>
<pre class='added' data-is-non-breaking="">
public class CKShareParticipant : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKShareParticipant (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareParticipant (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKShareParticipant (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantAcceptanceStatus AcceptanceStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantPermission Permission { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKShareParticipantType Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentity UserIdentity { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKShareParticipant -->
<div> <!-- start type CKShareParticipantAcceptanceStatus -->
<h3>New Type CloudKit.CKShareParticipantAcceptanceStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKShareParticipantAcceptanceStatus {
	<span class='added added-field ' data-is-non-breaking="">Accepted = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Pending = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Removed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type CKShareParticipantAcceptanceStatus -->
<div> <!-- start type CKShareParticipantPermission -->
<h3>New Type CloudKit.CKShareParticipantPermission</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKShareParticipantPermission {
	<span class='added added-field ' data-is-non-breaking="">None = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadOnly = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadWrite = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type CKShareParticipantPermission -->
<div> <!-- start type CKShareParticipantType -->
<h3>New Type CloudKit.CKShareParticipantType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CKShareParticipantType {
	<span class='added added-field ' data-is-non-breaking="">Owner = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">PrivateUser = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">PublicUser = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type CKShareParticipantType -->
<div> <!-- start type CKUserIdentity -->
<h3>New Type CloudKit.CKUserIdentity</h3>
<pre class='added' data-is-non-breaking="">
public class CKUserIdentity : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKUserIdentity (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentity (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentity (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasICloudAccount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKUserIdentityLookupInfo LookupInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPersonNameComponents NameComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordID UserRecordID { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type CKUserIdentity -->
<div> <!-- start type CKUserIdentityLookupInfo -->
<h3>New Type CloudKit.CKUserIdentityLookupInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CKUserIdentityLookupInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CKUserIdentityLookupInfo (CKRecordID userRecordID);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CKUserIdentityLookupInfo (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentityLookupInfo (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CKUserIdentityLookupInfo (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string EmailAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PhoneNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CKRecordID UserRecordID { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo FromEmail (string email);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo FromPhoneNumber (string phoneNumber);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo[] GetLookupInfos (CKRecordID[] recordIDs);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo[] GetLookupInfosWithEmails (string[] emails);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CKUserIdentityLookupInfo[] GetLookupInfosWithPhoneNumbers (string[] phoneNumbers);</span>
}
</pre>
</div> <!-- end type CKUserIdentityLookupInfo -->

</div> <!-- end namespace CloudKit -->
<!-- start namespace CoreAnimation --> <div> 
<h2>Namespace CoreAnimation</h2>
<!-- start type CAAnimationDelegate --> <div>
<h3>Type Changed: CoreAnimation.CAAnimationDelegate</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICAAnimationDelegate</span>
</pre>
</div>

</div> <!-- end type CAAnimationDelegate -->
<!-- start type CADisplayLink --> <div>
<h3>Type Changed: CoreAnimation.CADisplayLink</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PreferredFramesPerSecond { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TargetTimestamp { get; }</span>
</pre>
</div>

</div> <!-- end type CADisplayLink -->
<!-- start type CAEmitterBehavior --> <div>
<h3>Type Changed: CoreAnimation.CAEmitterBehavior</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SimpleAttractor { get; }</span>
</pre>
</div>

</div> <!-- end type CAEmitterBehavior -->
<!-- start type CALayer --> <div>
<h3>Type Changed: CoreAnimation.CALayer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CAContentsFormat ContentsFormat { get; set; }</span>
</pre>
</div>

</div> <!-- end type CALayer -->
<!-- start type CALayerDelegate --> <div>
<h3>Type Changed: CoreAnimation.CALayerDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillDrawLayer (CALayer layer);</span>
</pre>
</div>

</div> <!-- end type CALayerDelegate -->
<!-- start type CALayerDelegate_Extensions --> <div>
<h3>Type Changed: CoreAnimation.CALayerDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void WillDrawLayer (ICALayerDelegate This, CALayer layer);</span>
</pre>
</div>

</div> <!-- end type CALayerDelegate_Extensions -->
<div> <!-- start type CAAnimationDelegate_Extensions -->
<h3>New Type CoreAnimation.CAAnimationDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CAAnimationDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AnimationStarted (ICAAnimationDelegate This, CAAnimation anim);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void AnimationStopped (ICAAnimationDelegate This, CAAnimation anim, bool finished);</span>
}
</pre>
</div> <!-- end type CAAnimationDelegate_Extensions -->
<div> <!-- start type CAContentsFormat -->
<h3>New Type CoreAnimation.CAContentsFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CAContentsFormat {
	<span class='added added-field ' data-is-non-breaking="">Gray8Uint = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba16Float = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rgba8Uint = 1,</span>
}
</pre>
</div> <!-- end type CAContentsFormat -->
<div> <!-- start type CAContentsFormatExtensions -->
<h3>New Type CoreAnimation.CAContentsFormatExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class CAContentsFormatExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (CAContentsFormat self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CAContentsFormat GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type CAContentsFormatExtensions -->
<div> <!-- start type ICAAnimationDelegate -->
<h3>New Type CoreAnimation.ICAAnimationDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ICAAnimationDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ICAAnimationDelegate -->

</div> <!-- end namespace CoreAnimation -->
<!-- start namespace CoreBluetooth --> <div> 
<h2>Namespace CoreBluetooth</h2>
<!-- start type CBCentralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBCentralManager</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBManager</span>

</div> <!-- end type CBCentralManager -->
<!-- start type CBPeripheralManager --> <div>
<h3>Type Changed: CoreBluetooth.CBPeripheralManager</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>CoreBluetooth.CBManager</span>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CBPeripheralManager ();</span>
</pre>
</div>

</div> <!-- end type CBPeripheralManager -->
<!-- start type CBUUID --> <div>
<h3>Type Changed: CoreBluetooth.CBUUID</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CharacteristicValidRangeString { get; }</span>
</pre>
</div>

</div> <!-- end type CBUUID -->
<div> <!-- start type AdvertisementData -->
<h3>New Type CoreBluetooth.AdvertisementData</h3>
<pre class='added' data-is-non-breaking="">
public class AdvertisementData : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AdvertisementData (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? IsConnectable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string LocalName { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData ManufacturerData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] OverflowServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary&lt;CBUUID,Foundation.NSData&gt; ServiceData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] ServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBUUID[] SolicitedServiceUuids { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber TxPowerLevel { get; set; }</span>
}
</pre>
</div> <!-- end type AdvertisementData -->
<div> <!-- start type CBManager -->
<h3>New Type CoreBluetooth.CBManager</h3>
<pre class='added' data-is-non-breaking="">
public class CBManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected CBManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CBManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CBManagerState State { get; }</span>
}
</pre>
</div> <!-- end type CBManager -->
<div> <!-- start type CBManagerState -->
<h3>New Type CoreBluetooth.CBManagerState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CBManagerState {
	<span class='added added-field ' data-is-non-breaking="">PoweredOff = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">PoweredOn = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Resetting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unauthorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 2,</span>
}
</pre>
</div> <!-- end type CBManagerState -->
<div> <!-- start type RestoredState -->
<h3>New Type CoreBluetooth.RestoredState</h3>
<pre class='added' data-is-non-breaking="">
public class RestoredState : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RestoredState (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] Peripherals { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public PeripheralScanningOptions ScanOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CBPeripheral[] ScanServices { get; set; }</span>
}
</pre>
</div> <!-- end type RestoredState -->

</div> <!-- end namespace CoreBluetooth -->
<!-- start namespace CoreData --> <div> 
<h2>Namespace CoreData</h2>
<!-- start type NSEntityDescription --> <div>
<h3>Type Changed: CoreData.NSEntityDescription</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RenamingIdentifier { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Method InsertNewObjectForEntityForName is deprecated, please use InsertNewObject instead")]
	public static Foundation.NSObject InsertNewObjectForEntityForName (string entityName, NSManagedObjectContext context);</span>
</div></pre>

</div> <!-- end type NSEntityDescription -->
<!-- start type NSEntityMappingType --> <div>
<h3>Type Changed: CoreData.NSEntityMappingType</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	Copy = <span class='removed removed-inline removed-breaking-inline'>5</span> <span class='added '>4</span>
</div><div data-is-breaking="">	Transform = <span class='removed removed-inline removed-breaking-inline'>6</span> <span class='added '>5</span>
</div></pre>

</div> <!-- end type NSEntityMappingType -->
<!-- start type NSFetchRequest --> <div>
<h3>Type Changed: CoreData.NSFetchRequest</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual INSFetchRequestResult[] Execute (out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSFetchRequest -->
<!-- start type NSIncrementalStore --> <div>
<h3>Type Changed: CoreData.NSIncrementalStore</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public Foundation.NSObject IdentifierForNewStoreAtURL (Foundation.NSUrl <span class='removed removed-inline '>storeURL</span> <span class='added '>storeUrl</span>)
</div></pre>

</div> <!-- end type NSIncrementalStore -->
<!-- start type NSManagedObject --> <div>
<h3>Type Changed: CoreData.NSManagedObject</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSManagedObject (NSManagedObjectContext moc);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static bool ContextShouldIgnoreUnModeledPropertyChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FaultingState { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AwakeFromSnapshotEvents (NSSnapshotEventType flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSFetchRequest CreateFetchRequest ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSEntityDescription GetEntityDescription ();</span>
</pre>
</div>

</div> <!-- end type NSManagedObject -->
<!-- start type NSManagedObjectContext --> <div>
<h3>Type Changed: CoreData.NSManagedObjectContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AutomaticallyMergesChangesFromParent { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSQueryGenerationToken QueryGenerationToken { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SetQueryGenerationFromToken (NSQueryGenerationToken generation, out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectContext -->
<!-- start type NSManagedObjectID --> <div>
<h3>Type Changed: CoreData.NSManagedObjectID</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type NSManagedObjectID -->
<!-- start type NSMappingModel --> <div>
<h3>Type Changed: CoreData.NSMappingModel</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSMappingModel GetInferredMappingModel (NSManagedObjectModel source, NSManagedObjectModel destination, out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSMappingModel -->
<!-- start type NSMergePolicy --> <div>
<h3>Type Changed: CoreData.NSMergePolicy</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy ErrorPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy MergeByPropertyObjectTrumpPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy MergeByPropertyStoreTrumpPolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy OverwritePolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSMergePolicy RollbackPolicy { get; }</span>
</pre>
</div>

</div> <!-- end type NSMergePolicy -->
<!-- start type NSMigrationManager --> <div>
<h3>Type Changed: CoreData.NSMigrationManager</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual bool MigrateStoreFromUrl (Foundation.NSUrl <span class='removed removed-inline '>sourceURL</span> <span class='added '>sourceUrl</span>, string sStoreType, Foundation.NSDictionary sOptions, NSMappingModel mappings, Foundation.NSUrl <span class='removed removed-inline '>dURL</span> <span class='added '>dUrl</span>, string dStoreType, Foundation.NSDictionary dOptions, out Foundation.NSError error)
</div></pre>

</div> <!-- end type NSMigrationManager -->
<!-- start type NSPersistentStore --> <div>
<h3>Type Changed: CoreData.NSPersistentStore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool LoadMetadata (out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStore -->
<!-- start type NSPersistentStoreCoordinator --> <div>
<h3>Type Changed: CoreData.NSPersistentStoreCoordinator</h3>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual NSPersistentStore AddPersistentStoreWithType (Foundation.NSString storeType, string configuration, Foundation.NSUrl <span class='removed removed-inline '>storeURL</span> <span class='added '>storeUrl</span>, Foundation.NSDictionary options, out Foundation.NSError error)
</div><div data-is-non-breaking="">	public virtual NSPersistentStore MigratePersistentStore (NSPersistentStore store, Foundation.NSUrl <span class='removed removed-inline '>URL</span> <span class='added '>url</span>, Foundation.NSDictionary options, Foundation.NSString storeType, out Foundation.NSError error)
</div><div data-is-non-breaking="">	public virtual NSPersistentStore PersistentStoreForUrl (Foundation.NSUrl <span class='removed removed-inline '>URL</span> <span class='added '>url</span>)
</div><div data-is-non-breaking="">	public virtual bool ReplacePersistentStore (Foundation.NSUrl <span class='removed removed-inline '>destinationURL</span> <span class='added '>destinationUrl</span>, Foundation.NSDictionary destinationOptions, Foundation.NSUrl <span class='removed removed-inline '>sourceURL</span> <span class='added '>sourceUrl</span>, Foundation.NSDictionary sourceOptions, string storeType, out Foundation.NSError error)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddPersistentStore (NSPersistentStoreDescription storeDescription, System.Action&lt;NSPersistentStoreDescription,Foundation.NSError&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSPersistentStoreDescription&gt; AddPersistentStoreAsync (NSPersistentStoreDescription storeDescription);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; GetMetadata (string storeType, Foundation.NSUrl url, Foundation.NSDictionary options, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool SetMetadata (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; metadata, string storeType, Foundation.NSUrl url, Foundation.NSDictionary options, out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type NSPersistentStoreCoordinator -->
<!-- start type NSPropertyDescription --> <div>
<h3>Type Changed: CoreData.NSPropertyDescription</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string RenamingIdentifier { get; set; }</span>
</pre>
</div>

</div> <!-- end type NSPropertyDescription -->
<div> <!-- start type INSFetchRequestResult -->
<h3>New Type CoreData.INSFetchRequestResult</h3>
<pre class='added' data-is-non-breaking="">
public interface INSFetchRequestResult : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type INSFetchRequestResult -->
<div> <!-- start type MigrationErrorType -->
<h3>New Type CoreData.MigrationErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MigrationErrorType {
	<span class='added added-field ' data-is-non-breaking="">EntityMigrationPolicy = 134170,</span>
	<span class='added added-field ' data-is-non-breaking="">ExternalRecordImport = 134200,</span>
	<span class='added added-field ' data-is-non-breaking="">InferredMappingModel = 134190,</span>
	<span class='added added-field ' data-is-non-breaking="">Migration = 134110,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationCancelled = 134120,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationManagerDestinationStore = 134160,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationManagerSourceStore = 134150,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationMissingMappingModel = 134140,</span>
	<span class='added added-field ' data-is-non-breaking="">MigrationMissingSourceModel = 134130,</span>
}
</pre>
</div> <!-- end type MigrationErrorType -->
<div> <!-- start type NSExpressionDescription -->
<h3>New Type CoreData.NSExpressionDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSExpressionDescription : CoreData.NSPropertyDescription, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionDescription (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSExpressionDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSExpressionDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression Expression { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSAttributeType ResultType { get; set; }</span>
}
</pre>
</div> <!-- end type NSExpressionDescription -->
<div> <!-- start type NSFetchRequestExpression -->
<h3>New Type CoreData.NSFetchRequestExpression</h3>
<pre class='added' data-is-non-breaking="">
public class NSFetchRequestExpression : Foundation.NSExpression, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSFetchRequestExpression (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchRequestExpression (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSFetchRequestExpression (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression Context { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsCountOnly { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSExpression Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSFetchRequestExpression FromFetch (Foundation.NSExpression fetch, Foundation.NSExpression context, bool countOnly);</span>
}
</pre>
</div> <!-- end type NSFetchRequestExpression -->
<div> <!-- start type NSPersistentContainer -->
<h3>New Type CoreData.NSPersistentContainer</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentContainer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentContainer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentContainer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentContainer (string name);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentContainer (string name, NSManagedObjectModel model);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSUrl DefaultDirectoryUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectModel ManagedObjectModel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectContext NewBackgroundContext { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentStoreCoordinator PersistentStoreCoordinator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSPersistentStoreDescription[] PersistentStoreDescriptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSManagedObjectContext ViewContext { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentContainer GetPersistentContainer (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentContainer GetPersistentContainer (string name, NSManagedObjectModel model);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadPersistentStores (System.Action&lt;NSPersistentStoreDescription,Foundation.NSError&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSPersistentStoreDescription&gt; LoadPersistentStoresAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Perform (System.Action&lt;NSManagedObjectContext&gt; block);</span>
}
</pre>
</div> <!-- end type NSPersistentContainer -->
<div> <!-- start type NSPersistentStoreDescription -->
<h3>New Type CoreData.NSPersistentStoreDescription</h3>
<pre class='added' data-is-non-breaking="">
public class NSPersistentStoreDescription : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentStoreDescription (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSPersistentStoreDescription (Foundation.NSUrl url);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSPersistentStoreDescription (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Configuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IsReadOnly { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; Options { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldAddStoreAsynchronously { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldInferMappingModelAutomatically { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldMigrateStoreAutomatically { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; SqlitePragmas { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Timeout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Type { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl Url { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSPersistentStoreDescription GetPersistentStoreDescription (Foundation.NSUrl Url);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetOption (Foundation.NSObject option, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (Foundation.NSObject value, string name);</span>
}
</pre>
</div> <!-- end type NSPersistentStoreDescription -->
<div> <!-- start type NSQueryGenerationToken -->
<h3>New Type CoreData.NSQueryGenerationToken</h3>
<pre class='added' data-is-non-breaking="">
public class NSQueryGenerationToken : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSQueryGenerationToken ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSQueryGenerationToken (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSQueryGenerationToken (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSQueryGenerationToken CurrentToken { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type NSQueryGenerationToken -->
<div> <!-- start type NSSnapshotEventType -->
<h3>New Type CoreData.NSSnapshotEventType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSSnapshotEventType {
	<span class='added added-field ' data-is-non-breaking="">MergePolicy = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">Refresh = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Rollback = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoDeletion = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoInsertion = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UndoUpdate = 8,</span>
}
</pre>
</div> <!-- end type NSSnapshotEventType -->
<div> <!-- start type ObjectGraphManagementErrorType -->
<h3>New Type CoreData.ObjectGraphManagementErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ObjectGraphManagementErrorType {
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectContextLocking = 132000,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectExternalRelationship = 133010,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectMerge = 133020,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectReferentialIntegrity = 133000,</span>
	<span class='added added-field ' data-is-non-breaking="">PersistentStoreCoordinatorLocking = 132010,</span>
}
</pre>
</div> <!-- end type ObjectGraphManagementErrorType -->
<div> <!-- start type PersistentStoreErrorType -->
<h3>New Type CoreData.PersistentStoreErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PersistentStoreErrorType {
	<span class='added added-field ' data-is-non-breaking="">IncompatibleSchema = 134020,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompatibleVersionHash = 134100,</span>
	<span class='added added-field ' data-is-non-breaking="">IncompleteSave = 134040,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidType = 134000,</span>
	<span class='added added-field ' data-is-non-breaking="">Open = 134080,</span>
	<span class='added added-field ' data-is-non-breaking="">Operation = 134070,</span>
	<span class='added added-field ' data-is-non-breaking="">Save = 134030,</span>
	<span class='added added-field ' data-is-non-breaking="">SaveConflicts = 134050,</span>
	<span class='added added-field ' data-is-non-breaking="">Timeout = 134090,</span>
	<span class='added added-field ' data-is-non-breaking="">TypeMismatch = 134010,</span>
}
</pre>
</div> <!-- end type PersistentStoreErrorType -->
<div> <!-- start type UserInfo -->
<h3>New Type CoreData.UserInfo</h3>
<pre class='added' data-is-non-breaking="">
public class UserInfo : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UserInfo ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UserInfo (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public NSPersistentStore[] AffectedStoresForError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError[] DetailedErrors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSString KeyForValidationError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSManagedObject ObjectForValidationError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public NSMergeConflict[] PersistentStoreSaveConflicts { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSPredicate PredicateForValidationError { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSValue ValueForValidationError { get; set; }</span>
}
</pre>
</div> <!-- end type UserInfo -->
<div> <!-- start type UserInfoKeys -->
<h3>New Type CoreData.UserInfoKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class UserInfoKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AffectedStoresForErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DetailedErrorsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeyForValidationErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ObjectForValidationErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PersistentStoreSaveConflictsKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PredicateForValidationErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueForValidationErrorKey { get; }</span>
}
</pre>
</div> <!-- end type UserInfoKeys -->
<div> <!-- start type ValidationErrorType -->
<h3>New Type CoreData.ValidationErrorType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum ValidationErrorType {
	<span class='added added-field ' data-is-non-breaking="">DateTooLate = 1630,</span>
	<span class='added added-field ' data-is-non-breaking="">DateTooSoon = 1640,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDate = 1650,</span>
	<span class='added added-field ' data-is-non-breaking="">ManagedObjectValidation = 1550,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingMandatoryProperty = 1570,</span>
	<span class='added added-field ' data-is-non-breaking="">MultipleErrors = 1560,</span>
	<span class='added added-field ' data-is-non-breaking="">NumberTooLarge = 1610,</span>
	<span class='added added-field ' data-is-non-breaking="">NumberTooSmall = 1620,</span>
	<span class='added added-field ' data-is-non-breaking="">RelationshipDeniedDelete = 1600,</span>
	<span class='added added-field ' data-is-non-breaking="">RelationshipExceedsMaximumCount = 1590,</span>
	<span class='added added-field ' data-is-non-breaking="">RelationshipLacksMinimumCount = 1580,</span>
	<span class='added added-field ' data-is-non-breaking="">StringPatternMatching = 1680,</span>
	<span class='added added-field ' data-is-non-breaking="">StringTooLong = 1660,</span>
	<span class='added added-field ' data-is-non-breaking="">StringTooShort = 1670,</span>
}
</pre>
</div> <!-- end type ValidationErrorType -->

</div> <!-- end namespace CoreData -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGColorSpace --> <div>
<h3>Type Changed: CoreGraphics.CGColorSpace</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool IsWideGamutRgb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool SupportsOutput { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public Foundation.NSData GetIccData ();</span>
</pre>
</div>

</div> <!-- end type CGColorSpace -->
<!-- start type CGColorSpaceNames --> <div>
<h3>Type Changed: CoreGraphics.CGColorSpaceNames</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedLinearGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedLinearSrgb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ExtendedSrgb { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LinearGray { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString LinearSrgb { get; }</span>
</pre>
</div>

</div> <!-- end type CGColorSpaceNames -->
<div> <!-- start type CGColorConversionInfo -->
<h3>New Type CoreGraphics.CGColorConversionInfo</h3>
<pre class='added' data-is-non-breaking="">
public class CGColorConversionInfo : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionInfo (CGColorConversionOptions options, GColorConversionInfoTriple[] triples);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionInfo (CGColorSpace src, CGColorSpace dst);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionInfo (Foundation.NSDictionary options, GColorConversionInfoTriple[] triples);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr Handle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Dispose ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected virtual void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void ~CGColorConversionInfo ();</span>
}
</pre>
</div> <!-- end type CGColorConversionInfo -->
<div> <!-- start type CGColorConversionInfoTransformType -->
<h3>New Type CoreGraphics.CGColorConversionInfoTransformType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CGColorConversionInfoTransformType {
	<span class='added added-field ' data-is-non-breaking="">ApplySpace = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">FromSpace = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ToSpace = 1,</span>
}
</pre>
</div> <!-- end type CGColorConversionInfoTransformType -->
<div> <!-- start type CGColorConversionOptions -->
<h3>New Type CoreGraphics.CGColorConversionOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CGColorConversionOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CGColorConversionOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? BlackPointCompensation { get; set; }</span>
}
</pre>
</div> <!-- end type CGColorConversionOptions -->
<div> <!-- start type GColorConversionInfoTriple -->
<h3>New Type CoreGraphics.GColorConversionInfoTriple</h3>
<pre class='added' data-is-non-breaking="">
public struct GColorConversionInfoTriple {
	// fields
	<span class='added added-field ' data-is-non-breaking="">public CGColorRenderingIntent Intent;</span>
	<span class='added added-field ' data-is-non-breaking="">public CGColorSpace Space;</span>
	<span class='added added-field ' data-is-non-breaking="">public CGColorConversionInfoTransformType Transform;</span>
}
</pre>
</div> <!-- end type GColorConversionInfoTriple -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace CoreImage --> <div> 
<h2>Namespace CoreImage</h2>
<!-- start type CIColor --> <div>
<h3>Type Changed: CoreImage.CIColor</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColor (nfloat red, nfloat green, nfloat blue, CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIColor (nfloat red, nfloat green, nfloat blue, nfloat alpha, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor BlackColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor BlueColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor ClearColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor CyanColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor GrayColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor GreenColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor MagentaColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor RedColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor WhiteColor { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIColor YellowColor { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIColor FromRgb (nfloat red, nfloat green, nfloat blue, CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIColor FromRgba (nfloat red, nfloat green, nfloat blue, nfloat alpha, CoreGraphics.CGColorSpace colorSpace);</span>
</pre>
</div>

</div> <!-- end type CIColor -->
<!-- start type CIContext --> <div>
<h3>Type Changed: CoreImage.CIContext</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CIContext (CIContextOptions options);</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFormat WorkingFormat { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClearCaches ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGImage CreateCGImage (CIImage image, CoreGraphics.CGRect fromRect, CIFormat format, CoreGraphics.CGColorSpace colorSpace, bool deferred);</span>
</pre>
</div>

</div> <!-- end type CIContext -->
<!-- start type CIContextOptions --> <div>
<h3>Type Changed: CoreImage.CIContextOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? CacheIntermediates { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? OutputPremultiplied { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIContextOptions -->
<!-- start type CIDetectorOptions --> <div>
<h3>Type Changed: CoreImage.CIDetectorOptions</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CIImageOrientation? ImageOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? MaxFeatureCount { get; set; }</span>
</pre>
</div>

</div> <!-- end type CIDetectorOptions -->
<!-- start type CIFilter --> <div>
<h3>Type Changed: CoreImage.CIFilter</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual string Name { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSData data, CIRawFilterOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSData data, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSUrl url, CIRawFilterOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (Foundation.NSUrl url, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary properties, CIRawFilterOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFilter CreateRawFilter (CoreVideo.CVPixelBuffer pixelBuffer, Foundation.NSDictionary properties, Foundation.NSDictionary options);</span>
</pre>
</div>

</div> <!-- end type CIFilter -->
<!-- start type CIImage --> <div>
<h3>Type Changed: CoreImage.CIImage</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGImage CGImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByApplyingGaussianBlur (double sigma);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByClamping (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByColorMatchingColorSpaceToWorkingSpace (CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByColorMatchingWorkingSpaceToColorSpace (CoreGraphics.CGColorSpace colorSpace);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByPremultiplyingAlpha ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateBySettingAlphaOne (CoreGraphics.CGRect extent);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateBySettingProperties (Foundation.NSDictionary properties);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CIImage CreateByUnpremultiplyingAlpha ();</span>
</pre>
</div>

</div> <!-- end type CIImage -->
<div> <!-- start type CIClamp -->
<h3>New Type CoreImage.CIClamp</h3>
<pre class='added' data-is-non-breaking="">
public class CIClamp : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIClamp ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIClamp (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIClamp (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIClamp (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Extent { get; set; }</span>
}
</pre>
</div> <!-- end type CIClamp -->
<div> <!-- start type CIContext_ImageRepresentation -->
<h3>New Type CoreImage.CIContext_ImageRepresentation</h3>
<pre class='added' data-is-non-breaking="">
public static class CIContext_ImageRepresentation {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetJpegRepresentation (CIContext This, CIImage image, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSData GetTiffRepresentation (CIContext This, CIImage image, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WriteJpegRepresentation (CIContext This, CIImage image, Foundation.NSUrl url, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool WriteTiffRepresentation (CIContext This, CIImage image, Foundation.NSUrl url, CIFormat format, CoreGraphics.CGColorSpace colorSpace, Foundation.NSDictionary options, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CIContext_ImageRepresentation -->
<div> <!-- start type CIHueSaturationValueGradient -->
<h3>New Type CoreImage.CIHueSaturationValueGradient</h3>
<pre class='added' data-is-non-breaking="">
public class CIHueSaturationValueGradient : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIHueSaturationValueGradient ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIHueSaturationValueGradient (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIHueSaturationValueGradient (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIHueSaturationValueGradient (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColorSpace ColorSpace { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Dither { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Radius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Softness { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float Value { get; set; }</span>
}
</pre>
</div> <!-- end type CIHueSaturationValueGradient -->
<div> <!-- start type CIImageProcessorKernel -->
<h3>New Type CoreImage.CIImageProcessorKernel</h3>
<pre class='added' data-is-non-breaking="">
public class CIImageProcessorKernel : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIImageProcessorKernel ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageProcessorKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIImageProcessorKernel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CIFormat OutputFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static bool SynchronizeInputs { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static CIImage Apply (CoreGraphics.CGRect extent, CIImage[] inputs, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; args, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CIFormat GetFormat (int input);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetRegionOfInterest (int input, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; arguments, CoreGraphics.CGRect outputRect);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool Process (ICIImageProcessorInput[] inputs, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; arguments, ICIImageProcessorOutput output, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type CIImageProcessorKernel -->
<div> <!-- start type CINinePartStretched -->
<h3>New Type CoreImage.CINinePartStretched</h3>
<pre class='added' data-is-non-breaking="">
public class CINinePartStretched : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartStretched ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartStretched (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CINinePartStretched (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CINinePartStretched (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector GrowAmount { get; set; }</span>
}
</pre>
</div> <!-- end type CINinePartStretched -->
<div> <!-- start type CINinePartTiled -->
<h3>New Type CoreImage.CINinePartTiled</h3>
<pre class='added' data-is-non-breaking="">
public class CINinePartTiled : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartTiled ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CINinePartTiled (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CINinePartTiled (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CINinePartTiled (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector Breakpoint1 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool FlipYTiles { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector GrowAmount { get; set; }</span>
}
</pre>
</div> <!-- end type CINinePartTiled -->
<div> <!-- start type CIRawFilterOptions -->
<h3>New Type CoreImage.CIRawFilterOptions</h3>
<pre class='added' data-is-non-breaking="">
public class CIRawFilterOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIRawFilterOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIRawFilterOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSSet ActiveKeys { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? AllowDraftMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? BaselineExposure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? Boost { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? BoostShadowAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? ColorNoiseReductionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? DisableGamutMap { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? EnableChromaticNoiseTracking { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? EnableSharpening { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? EnableVendorLensCorrection { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? IgnoreImageOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? ImageOrientation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIFilter LinearSpaceFilter { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? LuminanceNoiseReductionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralChromaticityX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralChromaticityY { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector NeutralLocation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralTemperature { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? NeutralTint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionContrastAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionDetailAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public double? NoiseReductionSharpnessAmount { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public CIVector OutputNativeSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public float? ScaleFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSDictionary[] SupportedDecoderVersions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string Version { get; set; }</span>
}
</pre>
</div> <!-- end type CIRawFilterOptions -->
<div> <!-- start type CIThermal -->
<h3>New Type CoreImage.CIThermal</h3>
<pre class='added' data-is-non-breaking="">
public class CIThermal : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIThermal ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIThermal (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIThermal (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIThermal (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIThermal -->
<div> <!-- start type CIXRay -->
<h3>New Type CoreImage.CIXRay</h3>
<pre class='added' data-is-non-breaking="">
public class CIXRay : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public CIXRay ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public CIXRay (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIXRay (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected CIXRay (IntPtr handle);</span>
}
</pre>
</div> <!-- end type CIXRay -->
<div> <!-- start type ICIImageProcessorInput -->
<h3>New Type CoreImage.ICIImageProcessorInput</h3>
<pre class='added' data-is-non-breaking="">
public interface ICIImageProcessorInput : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BaseAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFormat Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLTexture MetalTexture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Region { get; }</span>
}
</pre>
</div> <!-- end type ICIImageProcessorInput -->
<div> <!-- start type ICIImageProcessorOutput -->
<h3>New Type CoreImage.ICIImageProcessorOutput</h3>
<pre class='added' data-is-non-breaking="">
public interface ICIImageProcessorOutput : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual IntPtr BaseAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint BytesPerRow { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CIFormat Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLCommandBuffer MetalCommandBuffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLTexture MetalTexture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreVideo.CVPixelBuffer PixelBuffer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Region { get; }</span>
}
</pre>
</div> <!-- end type ICIImageProcessorOutput -->

</div> <!-- end namespace CoreImage -->
<!-- start namespace CoreLocation --> <div> 
<h2>Namespace CoreLocation</h2>
<!-- start type CLLocation --> <div>
<h3>Type Changed: CoreLocation.CLLocation</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual string Description ();</span>
</pre>

</div> <!-- end type CLLocation -->
<!-- start type CLLocationCoordinate2D --> <div>
<h3>Type Changed: CoreLocation.CLLocationCoordinate2D</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type CLLocationCoordinate2D -->

</div> <!-- end namespace CoreLocation -->
<!-- start namespace CoreMedia --> <div> 
<h2>Namespace CoreMedia</h2>
<!-- start type CMBlockBuffer --> <div>
<h3>Type Changed: CoreMedia.CMBlockBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICMAttachmentBearer</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError AppendMemoryBlock (byte[] data, uint offsetToData, CMBlockBufferFlags flags);</span>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError CopyDataBytes (uint offsetToData, uint dataLength, out byte[] destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public static CMBlockBuffer FromMemoryBlock (byte[] data, uint offsetToData, CMBlockBufferFlags flags, out CMBlockBufferError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public CMBlockBufferError ReplaceDataBytes (byte[] sourceBytes, uint offsetIntoDestination);</span>
</pre>
</div>

</div> <!-- end type CMBlockBuffer -->
<!-- start type CMSampleBuffer --> <div>
<h3>Type Changed: CoreMedia.CMSampleBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ICMAttachmentBearer</span>
</pre>
</div>

</div> <!-- end type CMSampleBuffer -->
<div> <!-- start type CMAttachmentBearer -->
<h3>New Type CoreMedia.CMAttachmentBearer</h3>
<pre class='added' data-is-non-breaking="">
public static class CMAttachmentBearer {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static T GetAttachment&lt;T&gt; (ICMAttachmentBearer target, string key, out CMAttachmentMode attachmentModeOut);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary GetAttachments (ICMAttachmentBearer target, CMAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PropagateAttachments (ICMAttachmentBearer source, ICMAttachmentBearer destination);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAllAttachments (ICMAttachmentBearer target);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveAttachment (ICMAttachmentBearer target, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAttachment (ICMAttachmentBearer target, string key, ObjCRuntime.INativeObject value, CMAttachmentMode attachmentMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAttachments (ICMAttachmentBearer target, Foundation.NSDictionary theAttachments, CMAttachmentMode attachmentMode);</span>
}
</pre>
</div> <!-- end type CMAttachmentBearer -->
<div> <!-- start type CMAttachmentMode -->
<h3>New Type CoreMedia.CMAttachmentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum CMAttachmentMode {
	<span class='added added-field ' data-is-non-breaking="">ShouldNotPropagate = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ShouldPropagate = 1,</span>
}
</pre>
</div> <!-- end type CMAttachmentMode -->
<div> <!-- start type ICMAttachmentBearer -->
<h3>New Type CoreMedia.ICMAttachmentBearer</h3>
<pre class='added' data-is-non-breaking="">
public interface ICMAttachmentBearer : ObjCRuntime.INativeObject {
}
</pre>
</div> <!-- end type ICMAttachmentBearer -->

</div> <!-- end namespace CoreMedia -->
<!-- start namespace CoreText --> <div> 
<h2>Namespace CoreText</h2>
<!-- start type CTStringAttributeKey --> <div>
<h3>Type Changed: CoreText.CTStringAttributeKey</h3>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString BackgroundColor;</span>
	<span class='added added-field ' data-is-non-breaking="">public static Foundation.NSString HorizontalInVerticalForms;</span>
</pre>
</div>

</div> <!-- end type CTStringAttributeKey -->
<!-- start type CTStringAttributes --> <div>
<h3>Type Changed: CoreText.CTStringAttributes</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public CoreGraphics.CGColor BackgroundColor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int? HorizontalInVerticalForms { get; set; }</span>
</pre>
</div>

</div> <!-- end type CTStringAttributes -->

</div> <!-- end namespace CoreText -->
<!-- start namespace CoreVideo --> <div> 
<h2>Namespace CoreVideo</h2>
<!-- start type CVImageBuffer --> <div>
<h3>Type Changed: CoreVideo.CVImageBuffer</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TransferFunction_SMPTE_ST_428_1 { get; }</span>
</pre>
</div>

</div> <!-- end type CVImageBuffer -->
<!-- start type CVPixelFormatType --> <div>
<h3>Type Changed: CoreVideo.CVPixelFormatType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CV14BayerBggr = 1650943796,</span>
	<span class='added added-field ' data-is-non-breaking="">CV14BayerGbrg = 1734505012,</span>
	<span class='added added-field ' data-is-non-breaking="">CV14BayerGrbg = 1735549492,</span>
	<span class='added added-field ' data-is-non-breaking="">CV14BayerRggb = 1919379252,</span>
	<span class='added added-field ' data-is-non-breaking="">CV30RgbLePackedWideGamut = 1999843442,</span>
</pre>
</div>

</div> <!-- end type CVPixelFormatType -->
<!-- start type CVReturn --> <div>
<h3>Type Changed: CoreVideo.CVReturn</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Retry = -6692,</span>
</pre>
</div>

</div> <!-- end type CVReturn -->

</div> <!-- end namespace CoreVideo -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type DictionaryContainer --> <div>
<h3>Type Changed: Foundation.DictionaryContainer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected CoreGraphics.CGPoint? GetCGPointValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected CoreGraphics.CGRect? GetCGRectValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected CoreGraphics.CGSize? GetCGSizeValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected CoreMedia.CMTime? GetCMTimeValue (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected Foundation.NSDictionary&lt;TKey,TValue&gt; GetNSDictionary&lt;TKey, TValue&gt; (NSString key);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCGPointValue (NSString key, CoreGraphics.CGPoint? value);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCGRectValue (NSString key, CoreGraphics.CGRect? value);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCGSizeValue (NSString key, CoreGraphics.CGSize? value);</span>
	<span class='added added-method ' data-is-non-breaking="">protected void SetCMTimeValue (NSString key, CoreMedia.CMTime? value);</span>
</pre>
</div>

</div> <!-- end type DictionaryContainer -->
<!-- start type NSCharacterSet --> <div>
<h3>Type Changed: Foundation.NSCharacterSet</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSCharacterSet -->
<!-- start type NSCocoaError --> <div>
<h3>Type Changed: Foundation.NSCocoaError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CloudSharingConflictError = 5123,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingErrorMaximum = 5375,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingErrorMinimum = 5120,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingNetworkFailureError = 5120,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingNoPermissionError = 5124,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingOtherError = 5375,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingQuotaExceededError = 5121,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudSharingTooManyParticipantsError = 5122,</span>
</pre>
</div>

</div> <!-- end type NSCocoaError -->
<!-- start type NSCoder --> <div>
<h3>Type Changed: Foundation.NSCoder</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDecodingFailurePolicy DecodingFailurePolicy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSError Error { get; }</span>
</pre>
</div>

</div> <!-- end type NSCoder -->
<!-- start type NSDateComponentsFormatterUnitsStyle --> <div>
<h3>Type Changed: Foundation.NSDateComponentsFormatterUnitsStyle</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Brief = 5,</span>
</pre>
</div>

</div> <!-- end type NSDateComponentsFormatterUnitsStyle -->
<!-- start type NSDateIntervalFormatter --> <div>
<h3>Type Changed: Foundation.NSDateIntervalFormatter</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (NSDateInterval dateInterval);</span>
</pre>
</div>

</div> <!-- end type NSDateIntervalFormatter -->
<!-- start type NSDictionary`2 --> <div>
<h3>Type Changed: Foundation.NSDictionary`2</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("TKey and TValue are inversed and won't work unless both types are identical. Use the generic overload that takes a count parameter instead")]
	public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TKey[] objects, TValue[] keys);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TValue[] objects, TKey[] keys, nint count);</span>
</pre>
</div>

</div> <!-- end type NSDictionary`2 -->
<!-- start type NSExpression --> <div>
<h3>Type Changed: Foundation.NSExpression</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSExpressionCallbackHandler Block { get; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("ValueWithObject is deprecated, please use EvaluateWith instead.")]
	public virtual NSExpression ExpressionValueWithObject (NSObject obj, NSMutableDictionary context);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFormat (string, NSExpression[]) is deprecated, please use FromFormat (string, NSObject[]) instead.")]
	public static NSExpression FromFormat (string format, NSExpression[] parameters);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("FromFunction (NSExpressionHandler, NSExpression[]) is deprecated, please use FromFunction (NSExpressionCallbackHandler, NSExpression[]) instead.")]
	public static NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public virtual NSExpression ExpressionValueWithObject (NSObject <span class='removed removed-inline '>object1</span> <span class='added '>obj</span>, NSMutableDictionary context)
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject EvaluateWith (NSObject obj, NSMutableDictionary context);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFormat (string expressionFormat);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFormat (string format, NSObject[] parameters);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSExpression FromFunction (NSExpressionCallbackHandler target, NSExpression[] parameters);</span>
</pre>
</div>

</div> <!-- end type NSExpression -->
<!-- start type NSKeyedArchiver --> <div>
<h3>Type Changed: Foundation.NSKeyedArchiver</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSKeyedArchiver ();</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSData EncodedData { get; }</span>
</pre>
</div>

</div> <!-- end type NSKeyedArchiver -->
<!-- start type NSLocale --> <div>
<h3>Type Changed: Foundation.NSLocale</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string CalendarIdentifier { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual string GetLocalizedCalendarIdentifier (string calendarIdentifier);</span>
</pre>
</div>

</div> <!-- end type NSLocale -->
<!-- start type NSMutableAttributedString --> <div>
<h3>Type Changed: Foundation.NSMutableAttributedString</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMutableString MutableString { get; }</span>
</pre>
</div>

</div> <!-- end type NSMutableAttributedString -->
<!-- start type NSMutableCharacterSet --> <div>
<h3>Type Changed: Foundation.NSMutableCharacterSet</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSMutableCharacterSet -->
<!-- start type NSMutableDictionary`2 --> <div>
<h3>Type Changed: Foundation.NSMutableDictionary`2</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("TKey and TValue are inversed and won't work unless both types are identical. Use the generic overload that takes a count parameter instead")]
	public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TKey[] objects, TValue[] keys);</span>
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSMutableDictionary&lt;TKey,TValue&gt; FromObjectsAndKeys (TValue[] objects, TKey[] keys, nint count);</span>
</pre>
</div>

</div> <!-- end type NSMutableDictionary`2 -->
<!-- start type NSObject --> <div>
<h3>Type Changed: Foundation.NSObject</h3>
<p>Obsoleted fields:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-field' data-is-non-breaking="">[Obsolete ("Use PlatformAssembly for easier code sharing across platforms")]
	public static System.Reflection.Assembly MonoTouchAssembly;</span>
</div></pre>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static System.Reflection.Assembly PlatformAssembly;</span>
</pre>
</div>

</div> <!-- end type NSObject -->
<!-- start type NSPersonNameComponentsFormatter --> <div>
<h3>Type Changed: Foundation.NSPersonNameComponentsFormatter</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSPersonNameComponents GetComponents (string string);</span>
</pre>
</div>

</div> <!-- end type NSPersonNameComponentsFormatter -->
<!-- start type NSRunLoop --> <div>
<h3>Type Changed: Foundation.NSRunLoop</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Perform (System.Action block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Perform (NSString[] modes, System.Action block);</span>
</pre>
</div>

</div> <!-- end type NSRunLoop -->
<!-- start type NSStream --> <div>
<h3>Type Changed: Foundation.NSStream</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSString NetworkServiceTypeCallSignaling { get; }</span>
</pre>
</div>

</div> <!-- end type NSStream -->
<!-- start type NSTimer --> <div>
<h3>Type Changed: Foundation.NSTimer</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NSTimer (NSDate date, double seconds, bool repeats, System.Action&lt;NSTimer&gt; block);</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static NSTimer CreateScheduledTimer (double interval, bool repeats, System.Action&lt;NSTimer&gt; block);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSTimer CreateTimer (double interval, bool repeats, System.Action&lt;NSTimer&gt; block);</span>
</pre>
</div>

</div> <!-- end type NSTimer -->
<!-- start type NSUrl --> <div>
<h3>Type Changed: Foundation.NSUrl</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public int Port { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Equality (NSUrl x, NSUrl y);</span>
	<span class='added added-method ' data-is-non-breaking="">public static bool op_Inequality (NSUrl x, NSUrl y);</span>
</pre>
</div>

</div> <!-- end type NSUrl -->
<!-- start type NSUrlRequestNetworkServiceType --> <div>
<h3>Type Changed: Foundation.NSUrlRequestNetworkServiceType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">CallSignaling = 11,</span>
</pre>
</div>

</div> <!-- end type NSUrlRequestNetworkServiceType -->
<!-- start type NSUrlSessionTaskDelegate --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishCollectingMetrics (NSUrlSession session, NSUrlSessionTask task, NSUrlSessionTaskMetrics metrics);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate -->
<!-- start type NSUrlSessionTaskDelegate_Extensions --> <div>
<h3>Type Changed: Foundation.NSUrlSessionTaskDelegate_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void DidFinishCollectingMetrics (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSUrlSessionTaskMetrics metrics);</span>
</pre>
</div>

</div> <!-- end type NSUrlSessionTaskDelegate_Extensions -->
<!-- start type NSUserActivity --> <div>
<h3>Type Changed: Foundation.NSUserActivity</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use the constructor that allows you to set an activity type")]
	public NSUserActivity ();</span>
</div></pre>

</div> <!-- end type NSUserActivity -->
<!-- start type NSUserDefaults --> <div>
<h3>Type Changed: Foundation.NSUserDefaults</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static NSString DidChangeNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSString NoCloudAccountNotification { get; }</span>
</pre>
</div>

</div> <!-- end type NSUserDefaults -->
<div> <!-- start type NSDateInterval -->
<h3>New Type Foundation.NSDateInterval</h3>
<pre class='added' data-is-non-breaking="">
public class NSDateInterval : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDateInterval (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDateInterval (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval (NSDate startDate, NSDate endDate);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDateInterval (NSDate startDate, double duration);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSComparisonResult Compare (NSDateInterval dateInterval);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ContainsDate (NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Copy (NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDateInterval GetIntersection (NSDateInterval dateInterval);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Intersects (NSDateInterval dateInterval);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool IsEqualTo (NSDateInterval dateInterval);</span>
}
</pre>
</div> <!-- end type NSDateInterval -->
<div> <!-- start type NSDecodingFailurePolicy -->
<h3>New Type Foundation.NSDecodingFailurePolicy</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSDecodingFailurePolicy {
	<span class='added added-field ' data-is-non-breaking="">RaiseException = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SetErrorAndReturn = 1,</span>
}
</pre>
</div> <!-- end type NSDecodingFailurePolicy -->
<div> <!-- start type NSDimension -->
<h3>New Type Foundation.NSDimension</h3>
<pre class='added' data-is-non-breaking="">
public class NSDimension : Foundation.NSUnit, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSDimension (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDimension (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSDimension (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSDimension (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSDimension BaseUnit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUnitConverter Converter { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSDimension -->
<div> <!-- start type NSExpressionCallbackHandler -->
<h3>New Type Foundation.NSExpressionCallbackHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate NSExpressionCallbackHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSExpressionCallbackHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (NSObject evaluatedObject, NSExpression[] expressions, NSMutableDictionary context, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Invoke (NSObject evaluatedObject, NSExpression[] expressions, NSMutableDictionary context);</span>
}
</pre>
</div> <!-- end type NSExpressionCallbackHandler -->
<div> <!-- start type NSFileManager_NSUserInformation -->
<h3>New Type Foundation.NSFileManager_NSUserInformation</h3>
<pre class='added' data-is-non-breaking="">
public static class NSFileManager_NSUserInformation {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static NSUrl GetTemporaryDirectory (NSFileManager This);</span>
}
</pre>
</div> <!-- end type NSFileManager_NSUserInformation -->
<div> <!-- start type NSIso8601DateFormatOptions -->
<h3>New Type Foundation.NSIso8601DateFormatOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSIso8601DateFormatOptions {
	<span class='added added-field ' data-is-non-breaking="">ColonSeparatorInTime = 512,</span>
	<span class='added added-field ' data-is-non-breaking="">ColonSeparatorInTimeZone = 1024,</span>
	<span class='added added-field ' data-is-non-breaking="">DashSeparatorInDate = 256,</span>
	<span class='added added-field ' data-is-non-breaking="">Day = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">FullDate = 275,</span>
	<span class='added added-field ' data-is-non-breaking="">FullTime = 1632,</span>
	<span class='added added-field ' data-is-non-breaking="">InternetDateTime = 1907,</span>
	<span class='added added-field ' data-is-non-breaking="">Month = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SpaceBetweenDateAndTime = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">Time = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">TimeZone = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">WeekOfYear = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Year = 1,</span>
}
</pre>
</div> <!-- end type NSIso8601DateFormatOptions -->
<div> <!-- start type NSIso8601DateFormatter -->
<h3>New Type Foundation.NSIso8601DateFormatter</h3>
<pre class='added' data-is-non-breaking="">
public class NSIso8601DateFormatter : Foundation.NSFormatter, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSIso8601DateFormatter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSIso8601DateFormatter (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSIso8601DateFormatter (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSIso8601DateFormatter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSIso8601DateFormatOptions FormatOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSTimeZone TimeZone { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static string Format (NSDate date, NSTimeZone timeZone, NSIso8601DateFormatOptions formatOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSDate ToDate (string string);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (NSDate date);</span>
}
</pre>
</div> <!-- end type NSIso8601DateFormatter -->
<div> <!-- start type NSMeasurementFormatter -->
<h3>New Type Foundation.NSMeasurementFormatter</h3>
<pre class='added' data-is-non-breaking="">
public class NSMeasurementFormatter : Foundation.NSFormatter, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurementFormatter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurementFormatter (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurementFormatter (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurementFormatter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSLocale Locale { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSNumberFormatter NumberFormatter { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSMeasurementFormatterUnitOptions UnitOptions { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSFormattingUnitStyle UnitStyle { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (Foundation.NSMeasurement&lt;NSUnit&gt; measurement);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual string ToString (NSUnit unit);</span>
}
</pre>
</div> <!-- end type NSMeasurementFormatter -->
<div> <!-- start type NSMeasurementFormatterUnitOptions -->
<h3>New Type Foundation.NSMeasurementFormatterUnitOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum NSMeasurementFormatterUnitOptions {
	<span class='added added-field ' data-is-non-breaking="">NaturalScale = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">ProvidedUnit = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TemperatureWithoutUnit = 4,</span>
}
</pre>
</div> <!-- end type NSMeasurementFormatterUnitOptions -->
<div> <!-- start type NSMeasurement`1 -->
<h3>New Type Foundation.NSMeasurement`1</h3>
<pre class='added' data-is-non-breaking="">
public class NSMeasurement`1 : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurement`1 (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurement`1 (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSMeasurement`1 (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSMeasurement`1 (double doubleValue, NSUnit unit);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double DoubleValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUnit Unit { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanBeConvertedTo (NSUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Copy (NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;UnitType&gt; GetMeasurementByAdding (Foundation.NSMeasurement&lt;UnitType&gt; measurement);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;UnitType&gt; GetMeasurementByConverting (NSUnit unit);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSMeasurement&lt;UnitType&gt; GetMeasurementBySubtracting (Foundation.NSMeasurement&lt;UnitType&gt; measurement);</span>
}
</pre>
</div> <!-- end type NSMeasurement`1 -->
<div> <!-- start type NSUnit -->
<h3>New Type Foundation.NSUnit</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnit : Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnit ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnit (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnit (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnit (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnit (string symbol);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Symbol { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual NSObject Copy (NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnit -->
<div> <!-- start type NSUnitAcceleration -->
<h3>New Type Foundation.NSUnitAcceleration</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitAcceleration : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAcceleration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAcceleration (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAcceleration (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAcceleration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAcceleration (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAcceleration Gravity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAcceleration MetersPerSecondSquared { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitAcceleration -->
<div> <!-- start type NSUnitAngle -->
<h3>New Type Foundation.NSUnitAngle</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitAngle : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAngle ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAngle (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAngle (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitAngle (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitAngle (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle ArcMinutes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle ArcSeconds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Degrees { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Gradians { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Radians { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitAngle Revolutions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitAngle -->
<div> <!-- start type NSUnitArea -->
<h3>New Type Foundation.NSUnitArea</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitArea : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitArea ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitArea (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitArea (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitArea (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitArea (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea Acres { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea Ares { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea Hectares { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareCentimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareFeet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareInches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareKilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMegameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMicrometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareMillimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareNanometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitArea SquareYards { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitArea -->
<div> <!-- start type NSUnitConcentrationMass -->
<h3>New Type Foundation.NSUnitConcentrationMass</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitConcentrationMass : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConcentrationMass ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConcentrationMass (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConcentrationMass (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConcentrationMass (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConcentrationMass (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitConcentrationMass GramsPerLiter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitConcentrationMass MilligramsPerDeciliter { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static NSUnitConcentrationMass GetMillimolesPerLiter (double gramsPerMole);</span>
}
</pre>
</div> <!-- end type NSUnitConcentrationMass -->
<div> <!-- start type NSUnitConverter -->
<h3>New Type Foundation.NSUnitConverter</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitConverter : Foundation.NSObject, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverter ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverter (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual double GetBaseUnitValue (double value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual double GetValue (double baseUnitValue);</span>
}
</pre>
</div> <!-- end type NSUnitConverter -->
<div> <!-- start type NSUnitConverterLinear -->
<h3>New Type Foundation.NSUnitConverterLinear</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitConverterLinear : Foundation.NSUnitConverter, INSCoding, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverterLinear (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear (double coefficient);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitConverterLinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitConverterLinear (double coefficient, double constant);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Coefficient { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Constant { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitConverterLinear -->
<div> <!-- start type NSUnitDispersion -->
<h3>New Type Foundation.NSUnitDispersion</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitDispersion : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDispersion ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDispersion (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDispersion (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDispersion (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDispersion (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDispersion PartsPerMillion { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitDispersion -->
<div> <!-- start type NSUnitDuration -->
<h3>New Type Foundation.NSUnitDuration</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitDuration : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDuration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDuration (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDuration (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitDuration (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitDuration (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDuration Hours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDuration Minutes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitDuration Seconds { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitDuration -->
<div> <!-- start type NSUnitElectricCharge -->
<h3>New Type Foundation.NSUnitElectricCharge</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricCharge : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCharge ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCharge (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCharge (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCharge (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCharge (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge AmpereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge Coulombs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge KiloampereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge MegaampereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge MicroampereHours { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCharge MilliampereHours { get; }</span>
}
</pre>
</div> <!-- end type NSUnitElectricCharge -->
<div> <!-- start type NSUnitElectricCurrent -->
<h3>New Type Foundation.NSUnitElectricCurrent</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricCurrent : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCurrent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCurrent (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCurrent (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricCurrent (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricCurrent (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Amperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Kiloamperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Megaamperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Microamperes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricCurrent Milliamperes { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitElectricCurrent -->
<div> <!-- start type NSUnitElectricPotentialDifference -->
<h3>New Type Foundation.NSUnitElectricPotentialDifference</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricPotentialDifference : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricPotentialDifference ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricPotentialDifference (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricPotentialDifference (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricPotentialDifference (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricPotentialDifference (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Kilovolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Megavolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Microvolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Millivolts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricPotentialDifference Volts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitElectricPotentialDifference -->
<div> <!-- start type NSUnitElectricResistance -->
<h3>New Type Foundation.NSUnitElectricResistance</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitElectricResistance : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricResistance ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricResistance (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricResistance (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitElectricResistance (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitElectricResistance (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Kiloohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Megaohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Microohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Milliohms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitElectricResistance Ohms { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitElectricResistance -->
<div> <!-- start type NSUnitEnergy -->
<h3>New Type Foundation.NSUnitEnergy</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitEnergy : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitEnergy ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitEnergy (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitEnergy (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitEnergy (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitEnergy (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Calories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Joules { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Kilocalories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy Kilojoules { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitEnergy KilowattHours { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitEnergy -->
<div> <!-- start type NSUnitFrequency -->
<h3>New Type Foundation.NSUnitFrequency</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitFrequency : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFrequency ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFrequency (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFrequency (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFrequency (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFrequency (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Gigahertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Hertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Kilohertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Megahertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Microhertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Millihertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Nanohertz { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFrequency Terahertz { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitFrequency -->
<div> <!-- start type NSUnitFuelEfficiency -->
<h3>New Type Foundation.NSUnitFuelEfficiency</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitFuelEfficiency : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFuelEfficiency ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFuelEfficiency (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFuelEfficiency (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitFuelEfficiency (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitFuelEfficiency (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFuelEfficiency LitersPer100Kilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFuelEfficiency MilesPerGallon { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitFuelEfficiency MilesPerImperialGallon { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitFuelEfficiency -->
<div> <!-- start type NSUnitIlluminance -->
<h3>New Type Foundation.NSUnitIlluminance</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitIlluminance : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitIlluminance ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitIlluminance (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitIlluminance (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitIlluminance (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitIlluminance (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitIlluminance Lux { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitIlluminance -->
<div> <!-- start type NSUnitLength -->
<h3>New Type Foundation.NSUnitLength</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitLength : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitLength ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitLength (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitLength (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitLength (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitLength (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength AstronomicalUnits { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Centimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Decameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Decimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Fathoms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Feet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Furlongs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Hectometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Inches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Kilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Lightyears { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Megameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Meters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Micrometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Miles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Millimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Nanometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength NauticalMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Parsecs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Picometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength ScandinavianMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitLength Yards { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitLength -->
<div> <!-- start type NSUnitMass -->
<h3>New Type Foundation.NSUnitMass</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitMass : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitMass ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitMass (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitMass (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitMass (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitMass (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Carats { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Centigrams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Decigrams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Grams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Kilograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass MetricTons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Micrograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Milligrams { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Nanograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Ounces { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass OuncesTroy { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Picograms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass PoundsMass { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass ShortTons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Slugs { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitMass Stones { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitMass -->
<div> <!-- start type NSUnitPower -->
<h3>New Type Foundation.NSUnitPower</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitPower : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPower ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPower (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPower (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPower (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPower (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Femtowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Gigawatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Horsepower { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Kilowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Megawatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Microwatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Milliwatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Nanowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Picowatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Terawatts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPower Watts { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitPower -->
<div> <!-- start type NSUnitPressure -->
<h3>New Type Foundation.NSUnitPressure</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitPressure : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPressure ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPressure (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPressure (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitPressure (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitPressure (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Bars { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Gigapascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Hectopascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure InchesOfMercury { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Kilopascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Megapascals { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure Millibars { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure MillimetersOfMercury { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure NewtonsPerMetersSquared { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitPressure PoundsForcePerSquareInch { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitPressure -->
<div> <!-- start type NSUnitSpeed -->
<h3>New Type Foundation.NSUnitSpeed</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitSpeed : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitSpeed ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitSpeed (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitSpeed (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitSpeed (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitSpeed (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed KilometersPerHour { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed Knots { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed MetersPerSecond { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitSpeed MilesPerHour { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitSpeed -->
<div> <!-- start type NSUnitTemperature -->
<h3>New Type Foundation.NSUnitTemperature</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitTemperature : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitTemperature (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitTemperature (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitTemperature (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitTemperature (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitTemperature Celsius { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitTemperature Fahrenheit { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitTemperature Kelvin { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitTemperature -->
<div> <!-- start type NSUnitVolume -->
<h3>New Type Foundation.NSUnitVolume</h3>
<pre class='added' data-is-non-breaking="">
public class NSUnitVolume : Foundation.NSDimension, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitVolume ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitVolume (NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitVolume (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUnitVolume (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public NSUnitVolume (string symbol, NSUnitConverter converter);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume AcreFeet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Bushels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Centiliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicCentimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicDecimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicFeet { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicInches { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicKilometers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicMeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicMiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicMillimeters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume CubicYards { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Cups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Deciliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume FluidOunces { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Gallons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialFluidOunces { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialGallons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialPints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialQuarts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialTablespoons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume ImperialTeaspoons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Kiloliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Liters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Megaliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume MetricCups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Milliliters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Pints { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Quarts { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Tablespoons { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static NSUnitVolume Teaspoons { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (NSCoder encoder);</span>
}
</pre>
</div> <!-- end type NSUnitVolume -->
<div> <!-- start type NSUrlSessionTaskMetrics -->
<h3>New Type Foundation.NSUrlSessionTaskMetrics</h3>
<pre class='added' data-is-non-breaking="">
public class NSUrlSessionTaskMetrics : Foundation.NSObject, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUrlSessionTaskMetrics ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskMetrics (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskMetrics (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RedirectCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDateInterval TaskInterval { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlSessionTaskTransactionMetrics[] TransactionMetrics { get; }</span>
}
</pre>
</div> <!-- end type NSUrlSessionTaskMetrics -->
<div> <!-- start type NSUrlSessionTaskMetricsResourceFetchType -->
<h3>New Type Foundation.NSUrlSessionTaskMetricsResourceFetchType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum NSUrlSessionTaskMetricsResourceFetchType {
	<span class='added added-field ' data-is-non-breaking="">LocalCache = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkLoad = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">ServerPush = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type NSUrlSessionTaskMetricsResourceFetchType -->
<div> <!-- start type NSUrlSessionTaskTransactionMetrics -->
<h3>New Type Foundation.NSUrlSessionTaskTransactionMetrics</h3>
<pre class='added' data-is-non-breaking="">
public class NSUrlSessionTaskTransactionMetrics : Foundation.NSObject, INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NSUrlSessionTaskTransactionMetrics ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskTransactionMetrics (NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected NSUrlSessionTaskTransactionMetrics (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ConnectEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ConnectStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate DomainLookupEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate DomainLookupStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate FetchStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string NetworkProtocolName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ProxyConnection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlRequest Request { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate RequestEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate RequestStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlSessionTaskMetricsResourceFetchType ResourceFetchType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSUrlResponse Response { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ResponseEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate ResponseStartDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ReusedConnection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate SecureConnectionEndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual NSDate SecureConnectionStartDate { get; }</span>
}
</pre>
</div> <!-- end type NSUrlSessionTaskTransactionMetrics -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GLKit --> <div> 
<h2>Namespace GLKit</h2>
<!-- start type GLKTextureInfo --> <div>
<h3>Type Changed: GLKit.GLKTextureInfo</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ArrayLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Depth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MimapLevelCount { get; }</span>
</pre>
</div>

</div> <!-- end type GLKTextureInfo -->
<!-- start type GLKTextureLoader --> <div>
<h3>Type Changed: GLKit.GLKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginTextureLoad (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSNumber&gt; options, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback block);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSNumber&gt; options, CoreFoundation.DispatchQueue queue);</span>
	<span class='added added-method ' data-is-non-breaking="">public static GLKTextureInfo FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSNumber&gt; options, out Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type GLKTextureLoader -->
<!-- start type GLKTextureLoaderError --> <div>
<h3>Type Changed: GLKit.GLKTextureLoaderError</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">UnsupportedTextureTarget = 19,</span>
</pre>
</div>

</div> <!-- end type GLKTextureLoaderError -->

</div> <!-- end namespace GLKit -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKError --> <div>
<h3>Type Changed: GameKit.GKError</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">GameSessionRequestInvalid = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">MatchNotConnected = 28,</span>
</pre>
</div>

</div> <!-- end type GKError -->
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadRecentPlayers (System.Action&lt;GKPlayer[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKPlayer[]&gt; LoadRecentPlayersAsync ();</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKLocalPlayerListener --> <div>
<h3>Type Changed: GameKit.GKLocalPlayerListener</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use DidRequestMatch(GKPlayer player, GKPlayer[] recipientPlayers) instead")]
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayerListener -->
<!-- start type GKPlayer --> <div>
<h3>Type Changed: GameKit.GKPlayer</h3>
Modified base type: <span class='removed removed-inline removed-breaking-inline'>Foundation.NSObject</span> <span class='added '>GameKit.GKBasePlayer</span>

</div> <!-- end type GKPlayer -->
<h3>Removed Type <span class='breaking' data-is-breaking="">GameKit.GKPeerPickerConnectionType</span></h3><div> <!-- start type GKBasePlayer -->
<h3>New Type GameKit.GKBasePlayer</h3>
<pre class='added' data-is-non-breaking="">
public class GKBasePlayer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKBasePlayer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKBasePlayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKBasePlayer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PlayerID { get; }</span>
}
</pre>
</div> <!-- end type GKBasePlayer -->
<div> <!-- start type GKCloudPlayer -->
<h3>New Type GameKit.GKCloudPlayer</h3>
<pre class='added' data-is-non-breaking="">
public class GKCloudPlayer : GameKit.GKBasePlayer, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKCloudPlayer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCloudPlayer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKCloudPlayer (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void GetCurrentSignedInPlayer (string containerName, System.Action&lt;GKCloudPlayer,Foundation.NSError&gt; handler);</span>
}
</pre>
</div> <!-- end type GKCloudPlayer -->
<div> <!-- start type GKConnectionState -->
<h3>New Type GameKit.GKConnectionState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKConnectionState {
	<span class='added added-field ' data-is-non-breaking="">Connected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotConnected = 0,</span>
}
</pre>
</div> <!-- end type GKConnectionState -->
<div> <!-- start type GKGameSession -->
<h3>New Type GameKit.GKGameSession</h3>
<pre class='added' data-is-non-breaking="">
public class GKGameSession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKGameSession ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSession (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer[] BadgedPlayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate LastModifiedDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer LastModifiedPlayer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint MaxNumberOfConnectedPlayers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer Owner { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKCloudPlayer[] Players { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddEventListener (IGKGameSessionEventListener listener);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClearBadge (GKCloudPlayer[] players, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ClearBadgeAsync (GKCloudPlayer[] players);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void CreateSession (string containerName, string title, nint maxPlayers, System.Action&lt;GKGameSession,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKGameSession&gt; CreateSessionAsync (string containerName, string title, nint maxPlayers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual GKCloudPlayer[] GetPlayers (GKConnectionState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetShareUrl (System.Action&lt;Foundation.NSUrl,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSUrl&gt; GetShareUrlAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LoadData (System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; LoadDataAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadSession (string identifier, System.Action&lt;GKGameSession,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKGameSession&gt; LoadSessionAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadSessions (string containerName, System.Action&lt;GKGameSession[],Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;GKGameSession[]&gt; LoadSessionsAsync (string containerName);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveEventListener (IGKGameSessionEventListener listener);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RemoveSession (string identifier, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task RemoveSessionAsync (string identifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SaveData (Foundation.NSData data, System.Action&lt;Foundation.NSData,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSData&gt; SaveDataAsync (Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendData (Foundation.NSData data, GKTransportType transport, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendDataAsync (Foundation.NSData data, GKTransportType transport);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SendMessage (string key, string[] arguments, Foundation.NSData data, GKCloudPlayer[] players, bool badgePlayers, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SendMessageAsync (string key, string[] arguments, Foundation.NSData data, GKCloudPlayer[] players, bool badgePlayers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetConnectionState (GKConnectionState state, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task SetConnectionStateAsync (GKConnectionState state);</span>
}
</pre>
</div> <!-- end type GKGameSession -->
<div> <!-- start type GKGameSessionErrorCode -->
<h3>New Type GameKit.GKGameSessionErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKGameSessionErrorCode {
	<span class='added added-field ' data-is-non-breaking="">BadContainer = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudDriveDisabled = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudQuotaExceeded = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">ConnectionCancelledByUser = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">ConnectionFailed = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidSession = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkFailure = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAuthenticated = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SendDataNoRecipients = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">SendDataNotConnected = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">SendDataNotReachable = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">SendRateLimitReached = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">SessionConflict = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SessionHasMaxConnectedPlayers = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SessionNotShared = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 1,</span>
}
</pre>
</div> <!-- end type GKGameSessionErrorCode -->
<div> <!-- start type GKGameSessionErrorCodeExtensions -->
<h3>New Type GameKit.GKGameSessionErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class GKGameSessionErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (GKGameSessionErrorCode self);</span>
}
</pre>
</div> <!-- end type GKGameSessionErrorCodeExtensions -->
<div> <!-- start type GKGameSessionEventListener_Extensions -->
<h3>New Type GameKit.GKGameSessionEventListener_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class GKGameSessionEventListener_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddPlayer (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidChangeConnectionState (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player, GKConnectionState newState);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidReceiveData (IGKGameSessionEventListener This, GKGameSession session, Foundation.NSData data, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidReceiveMessage (IGKGameSessionEventListener This, GKGameSession session, string message, Foundation.NSData data, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemovePlayer (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidSaveData (IGKGameSessionEventListener This, GKGameSession session, GKCloudPlayer player, Foundation.NSData data);</span>
}
</pre>
</div> <!-- end type GKGameSessionEventListener_Extensions -->
<div> <!-- start type GKGameSessionSharingViewController -->
<h3>New Type GameKit.GKGameSessionSharingViewController</h3>
<pre class='added' data-is-non-breaking="">
public class GKGameSessionSharingViewController : UIKit.UIViewController, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKGameSessionSharingViewController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGameSessionSharingViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSessionSharingViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGameSessionSharingViewController (GKGameSession session);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSessionSharingViewController (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGameSessionSharingViewController (string nibName, Foundation.NSBundle bundle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IGKGameSessionSharingViewControllerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual GKGameSession Session { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type GKGameSessionSharingViewController -->
<div> <!-- start type GKGameSessionSharingViewControllerDelegate -->
<h3>New Type GameKit.GKGameSessionSharingViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class GKGameSessionSharingViewControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IGKGameSessionSharingViewControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSessionSharingViewControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSessionSharingViewControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKGameSessionSharingViewControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (GKGameSessionSharingViewController viewController, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type GKGameSessionSharingViewControllerDelegate -->
<div> <!-- start type GKTransportType -->
<h3>New Type GameKit.GKTransportType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum GKTransportType {
	<span class='added added-field ' data-is-non-breaking="">Reliable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unreliable = 0,</span>
}
</pre>
</div> <!-- end type GKTransportType -->
<div> <!-- start type IGKGameSessionEventListener -->
<h3>New Type GameKit.IGKGameSessionEventListener</h3>
<pre class='added' data-is-non-breaking="">
public interface IGKGameSessionEventListener : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IGKGameSessionEventListener -->
<div> <!-- start type IGKGameSessionSharingViewControllerDelegate -->
<h3>New Type GameKit.IGKGameSessionSharingViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IGKGameSessionSharingViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (GKGameSessionSharingViewController viewController, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type IGKGameSessionSharingViewControllerDelegate -->

</div> <!-- end namespace GameKit -->
<!-- start namespace GameplayKit --> <div> 
<h2>Namespace GameplayKit</h2>
<!-- start type GKAgent --> <div>
<h3>Type Changed: GameplayKit.GKAgent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKAgent (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>

</div> <!-- end type GKAgent -->
<!-- start type GKAgent2D --> <div>
<h3>Type Changed: GameplayKit.GKAgent2D</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKAgent2D (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>

</div> <!-- end type GKAgent2D -->
<!-- start type GKBehavior --> <div>
<h3>Type Changed: GameplayKit.GKBehavior</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type GKBehavior -->
<!-- start type GKComponent --> <div>
<h3>Type Changed: GameplayKit.GKComponent</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">protected GKComponent (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKComponent -->
<!-- start type GKEntity --> <div>
<h3>Type Changed: GameplayKit.GKEntity</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKEntity (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKEntity -->
<!-- start type GKGraph --> <div>
<h3>Type Changed: GameplayKit.GKGraph</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraph (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKGraph -->
<!-- start type GKGraphNode --> <div>
<h3>Type Changed: GameplayKit.GKGraphNode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraphNode (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKGraphNode -->
<!-- start type GKGraphNode2D --> <div>
<h3>Type Changed: GameplayKit.GKGraphNode2D</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGraphNode2D (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>

</div> <!-- end type GKGraphNode2D -->
<!-- start type GKGridGraph --> <div>
<h3>Type Changed: GameplayKit.GKGridGraph</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGridGraph (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>

</div> <!-- end type GKGridGraph -->
<!-- start type GKGridGraphNode --> <div>
<h3>Type Changed: GameplayKit.GKGridGraphNode</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKGridGraphNode (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>

</div> <!-- end type GKGridGraphNode -->
<!-- start type GKObstacleGraph --> <div>
<h3>Type Changed: GameplayKit.GKObstacleGraph</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKObstacleGraph (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>

</div> <!-- end type GKObstacleGraph -->
<!-- start type GKPolygonObstacle --> <div>
<h3>Type Changed: GameplayKit.GKPolygonObstacle</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public GKPolygonObstacle (Foundation.NSCoder coder);</span>
</pre>
</div>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCoding</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
</pre>
</div>

</div> <!-- end type GKPolygonObstacle -->
<!-- start type GKQuadTree --> <div>
<h3>Type Changed: GameplayKit.GKQuadTree</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use constructor with the same signature")]
	public static GKQuadTree QuadTreeWithMinPosition (OpenTK.Vector2 min, OpenTK.Vector2 max, float minCellSize);</span>
</div></pre>

</div> <!-- end type GKQuadTree -->
<!-- start type GKQuadTreeNode --> <div>
<h3>Type Changed: GameplayKit.GKQuadTreeNode</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Valid instance of this type cannot be directly created")]
	public GKQuadTreeNode ();</span>
</div></pre>

</div> <!-- end type GKQuadTreeNode -->

</div> <!-- end namespace GameplayKit -->
<!-- start namespace ImageIO --> <div> 
<h2>Namespace ImageIO</h2>
<!-- start type CGImageDestinationOptions --> <div>
<h3>Type Changed: ImageIO.CGImageDestinationOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? OptimizeColorForSharing { get; set; }</span>
</pre>
</div>

</div> <!-- end type CGImageDestinationOptions -->
<!-- start type CGImageDestinationOptionsKeys --> <div>
<h3>Type Changed: ImageIO.CGImageDestinationOptionsKeys</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptimizeColorForSharing { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageDestinationOptionsKeys -->
<!-- start type CGImageProperties --> <div>
<h3>Type Changed: ImageIO.CGImageProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGAsShotNeutral { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGAsShotWhiteXY { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBaselineExposure { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBaselineNoise { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBaselineSharpness { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGBlackLevel { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCalibrationIlluminant1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCalibrationIlluminant2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCameraCalibration1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCameraCalibration2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGCameraCalibrationSignature { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGColorMatrix1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGColorMatrix2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGFixVignetteRadial { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGNoiseProfile { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGPrivateData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGProfileCalibrationSignature { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGWarpFisheye { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGWarpRectilinear { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DNGWhiteLevel { get; }</span>
</pre>
</div>

</div> <!-- end type CGImageProperties -->

</div> <!-- end namespace ImageIO -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKCoordinateRegion --> <div>
<h3>Type Changed: MapKit.MKCoordinateRegion</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type MKCoordinateRegion -->
<!-- start type MKCoordinateSpan --> <div>
<h3>Type Changed: MapKit.MKCoordinateSpan</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override string ToString ();</span>
</pre>
</div>

</div> <!-- end type MKCoordinateSpan -->
<!-- start type MKMapView --> <div>
<h3>Type Changed: MapKit.MKMapView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShowsScale { get; set; }</span>
</pre>
</div>

</div> <!-- end type MKMapView -->
<!-- start type MKPlacemark --> <div>
<h3>Type Changed: MapKit.MKPlacemark</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MKPlacemark (CoreLocation.CLLocationCoordinate2D coordinate);</span>
</pre>
</div>

</div> <!-- end type MKPlacemark -->
<div> <!-- start type MKOverlayView -->
<h3>New Type MapKit.MKOverlayView</h3>
<pre class='added' data-is-non-breaking="">
public class MKOverlayView {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MKOverlayView ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static nfloat MKRoadWidthAtZoomScale (nfloat zoomScale);</span>
}
</pre>
</div> <!-- end type MKOverlayView -->
<div> <!-- start type NSUserActivity_MKMapItem -->
<h3>New Type MapKit.NSUserActivity_MKMapItem</h3>
<pre class='added' data-is-non-breaking="">
public static class NSUserActivity_MKMapItem {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MKMapItem GetMapItem (Foundation.NSUserActivity This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetMapItem (Foundation.NSUserActivity This, MKMapItem item);</span>
}
</pre>
</div> <!-- end type NSUserActivity_MKMapItem -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MediaPlayer --> <div> 
<h2>Namespace MediaPlayer</h2>
<!-- start type MPChangeLanguageOptionCommandEvent --> <div>
<h3>Type Changed: MediaPlayer.MPChangeLanguageOptionCommandEvent</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangeLanguageOptionSetting Setting { get; }</span>
</pre>
</div>

</div> <!-- end type MPChangeLanguageOptionCommandEvent -->
<!-- start type MPNowPlayingInfoCenter --> <div>
<h3>Type Changed: MediaPlayer.MPNowPlayingInfoCenter</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyCollectionIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyExternalContentIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyExternalUserProfileIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyIsLiveStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyMediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PropertyPlaybackProgress { get; }</span>
</pre>
</div>

</div> <!-- end type MPNowPlayingInfoCenter -->
<!-- start type MPRemoteCommandCenter --> <div>
<h3>Type Changed: MediaPlayer.MPRemoteCommandCenter</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Use MPRemoteCommandCenter.Shared")]
	public MPRemoteCommandCenter ();</span>
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangeRepeatModeCommand ChangeRepeatModeCommand { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPChangeShuffleModeCommand ChangeShuffleModeCommand { get; }</span>
</pre>
</div>

</div> <!-- end type MPRemoteCommandCenter -->
<div> <!-- start type MPChangeLanguageOptionSetting -->
<h3>New Type MediaPlayer.MPChangeLanguageOptionSetting</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPChangeLanguageOptionSetting {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">NowPlayingItemOnly = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Permanent = 2,</span>
}
</pre>
</div> <!-- end type MPChangeLanguageOptionSetting -->
<div> <!-- start type MPChangeRepeatModeCommand -->
<h3>New Type MediaPlayer.MPChangeRepeatModeCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeRepeatModeCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRepeatType CurrentRepeatType { get; set; }</span>
}
</pre>
</div> <!-- end type MPChangeRepeatModeCommand -->
<div> <!-- start type MPChangeRepeatModeCommandEvent -->
<h3>New Type MediaPlayer.MPChangeRepeatModeCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeRepeatModeCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeRepeatModeCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreservesRepeatMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPRepeatType RepeatType { get; }</span>
}
</pre>
</div> <!-- end type MPChangeRepeatModeCommandEvent -->
<div> <!-- start type MPChangeShuffleModeCommand -->
<h3>New Type MediaPlayer.MPChangeShuffleModeCommand</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeShuffleModeCommand : MediaPlayer.MPRemoteCommand, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommand (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommand (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPShuffleType CurrentShuffleType { get; set; }</span>
}
</pre>
</div> <!-- end type MPChangeShuffleModeCommand -->
<div> <!-- start type MPChangeShuffleModeCommandEvent -->
<h3>New Type MediaPlayer.MPChangeShuffleModeCommandEvent</h3>
<pre class='added' data-is-non-breaking="">
public class MPChangeShuffleModeCommandEvent : MediaPlayer.MPRemoteCommandEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommandEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPChangeShuffleModeCommandEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PreservesShuffleMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPShuffleType ShuffleType { get; }</span>
}
</pre>
</div> <!-- end type MPChangeShuffleModeCommandEvent -->
<div> <!-- start type MPErrorCodeExtensions -->
<h3>New Type MediaPlayer.MPErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MPErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MPErrorCode self);</span>
}
</pre>
</div> <!-- end type MPErrorCodeExtensions -->
<div> <!-- start type MPMediaItemArtwork -->
<h3>New Type MediaPlayer.MPMediaItemArtwork</h3>
<pre class='added' data-is-non-breaking="">
public class MPMediaItemArtwork : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItemArtwork (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPMediaItemArtwork (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItemArtwork (UIKit.UIImage image);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPMediaItemArtwork (CoreGraphics.CGSize boundsSize, System.Func&lt;CoreGraphics.CGSize,UIKit.UIImage&gt; requestHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Bounds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect ImageCropRectangle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual UIKit.UIImage ImageWithSize (CoreGraphics.CGSize size);</span>
}
</pre>
</div> <!-- end type MPMediaItemArtwork -->
<div> <!-- start type MPNowPlayingInfoMediaType -->
<h3>New Type MediaPlayer.MPNowPlayingInfoMediaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPNowPlayingInfoMediaType {
	<span class='added added-field ' data-is-non-breaking="">Audio = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type MPNowPlayingInfoMediaType -->
<div> <!-- start type MPRepeatType -->
<h3>New Type MediaPlayer.MPRepeatType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPRepeatType {
	<span class='added added-field ' data-is-non-breaking="">All = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">One = 1,</span>
}
</pre>
</div> <!-- end type MPRepeatType -->
<div> <!-- start type MPShuffleType -->
<h3>New Type MediaPlayer.MPShuffleType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPShuffleType {
	<span class='added added-field ' data-is-non-breaking="">Collections = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Items = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
}
</pre>
</div> <!-- end type MPShuffleType -->

</div> <!-- end namespace MediaPlayer -->
<!-- start namespace Metal --> <div> 
<h2>Namespace Metal</h2>
<!-- start type MTLVertexDescriptor --> <div>
<h3>Type Changed: Metal.MTLVertexDescriptor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MTLVertexDescriptor FromModelIO (ModelIO.MDLVertexDescriptor descriptor, out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type MTLVertexDescriptor -->

</div> <!-- end namespace Metal -->
<!-- start namespace MetalKit --> <div> 
<h2>Namespace MetalKit</h2>
<!-- start type MTKMeshBuffer --> <div>
<h3>Type Changed: MetalKit.MTKMeshBuffer</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ModelIO.IMDLNamed</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTKMeshBuffer -->
<!-- start type MTKTextureLoader --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLTexture FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public Metal.IMTLTexture FromName (string name, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromNames (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromNames (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromTexture (ModelIO.MDLTexture texture, Foundation.NSDictionary options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLTexture FromTexture (ModelIO.MDLTexture texture, Foundation.NSDictionary options, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromTexture (ModelIO.MDLTexture texture, MTKTextureLoaderOptions options, MTKTextureLoaderCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public Metal.IMTLTexture FromTexture (ModelIO.MDLTexture texture, MTKTextureLoaderOptions options, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FromUrls (Foundation.NSUrl[] urls, Foundation.NSDictionary options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Metal.IMTLTexture[] FromUrls (Foundation.NSUrl[] urls, Foundation.NSDictionary options, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public void FromUrls (Foundation.NSUrl[] urls, MTKTextureLoaderOptions options, MTKTextureLoaderArrayCallback completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public Metal.IMTLTexture[] FromUrls (Foundation.NSUrl[] urls, MTKTextureLoaderOptions options, out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoader -->
<!-- start type MTKTextureLoaderOptions --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoaderOptions</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public bool? AllocateMipmaps { get; <span class='added '>set;</span> }
</div><div data-is-non-breaking="">	public bool? Srgb { get; <span class='added '>set;</span> }
</div></pre>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public MTKTextureLoaderCubeLayout? CubeLayout { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool? GenerateMipmaps { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MTKTextureLoaderOrigin? Origin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Metal.MTLStorageMode? TextureStorageMode { get; set; }</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoaderOptions -->
<!-- start type MTKView --> <div>
<h3>Type Changed: MetalKit.MTKView</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">CoreAnimation.ICALayerDelegate</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ActionForLayer (CoreAnimation.CALayer layer, string eventKey);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DisplayLayer (CoreAnimation.CALayer layer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DrawLayer (CoreAnimation.CALayer layer, CoreGraphics.CGContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LayoutSublayersOfLayer (CoreAnimation.CALayer layer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillDrawLayer (CoreAnimation.CALayer layer);</span>
</pre>
</div>

</div> <!-- end type MTKView -->
<div> <!-- start type MTKTextureLoaderArrayCallback -->
<h3>New Type MetalKit.MTKTextureLoaderArrayCallback</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MTKTextureLoaderArrayCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MTKTextureLoaderArrayCallback (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Metal.IMTLTexture[] textures, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Metal.IMTLTexture[] textures, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderArrayCallback -->
<div> <!-- start type MTKTextureLoaderCubeLayout -->
<h3>New Type MetalKit.MTKTextureLoaderCubeLayout</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTKTextureLoaderCubeLayout {
	<span class='added added-field ' data-is-non-breaking="">Vertical = 0,</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderCubeLayout -->
<div> <!-- start type MTKTextureLoaderCubeLayoutExtensions -->
<h3>New Type MetalKit.MTKTextureLoaderCubeLayoutExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTKTextureLoaderCubeLayoutExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (MTKTextureLoaderCubeLayout self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTKTextureLoaderCubeLayout GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderCubeLayoutExtensions -->
<div> <!-- start type MTKTextureLoaderOrigin -->
<h3>New Type MetalKit.MTKTextureLoaderOrigin</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MTKTextureLoaderOrigin {
	<span class='added added-field ' data-is-non-breaking="">BottomLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">FlippedVertically = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TopLeft = 0,</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderOrigin -->
<div> <!-- start type MTKTextureLoaderOriginExtensions -->
<h3>New Type MetalKit.MTKTextureLoaderOriginExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MTKTextureLoaderOriginExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (MTKTextureLoaderOrigin self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MTKTextureLoaderOrigin GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type MTKTextureLoaderOriginExtensions -->

</div> <!-- end namespace MetalKit -->
<!-- start namespace MetalPerformanceShaders --> <div> 
<h2>Namespace MetalPerformanceShaders</h2>
<div> <!-- start type MPSAlphaType -->
<h3>New Type MetalPerformanceShaders.MPSAlphaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSAlphaType {
	<span class='added added-field ' data-is-non-breaking="">AlphaIsOne = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonPremultiplied = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Premultiplied = 2,</span>
}
</pre>
</div> <!-- end type MPSAlphaType -->
<div> <!-- start type MPSCnnConvolution -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolution</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolution : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolution (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolution (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnConvolution (Metal.IMTLDevice device, MPSCnnConvolutionDescriptor convolutionDescriptor, float[] kernelWeights, float[] biasTerms, MPSCnnConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuron Neuron { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnConvolution -->
<div> <!-- start type MPSCnnConvolutionDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnConvolutionDescriptor : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnConvolutionDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Groups { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint InputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSCnnNeuron Neuron { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint OutputFeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSCnnConvolutionDescriptor GetConvolutionDescriptor (uint kernelWidth, uint kernelHeight, uint inputFeatureChannels, uint outputFeatureChannels, MPSCnnNeuron neuronFilter);</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionDescriptor -->
<div> <!-- start type MPSCnnConvolutionFlags -->
<h3>New Type MetalPerformanceShaders.MPSCnnConvolutionFlags</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSCnnConvolutionFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type MPSCnnConvolutionFlags -->
<div> <!-- start type MPSCnnCrossChannelNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnCrossChannelNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnCrossChannelNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnCrossChannelNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnCrossChannelNormalization (Metal.IMTLDevice device, uint kernelSize);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelSize { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnCrossChannelNormalization -->
<div> <!-- start type MPSCnnFullyConnected -->
<h3>New Type MetalPerformanceShaders.MPSCnnFullyConnected</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnFullyConnected : MetalPerformanceShaders.MPSCnnConvolution, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnected (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnFullyConnected (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnFullyConnected (Metal.IMTLDevice device, MPSCnnConvolutionDescriptor convolutionDescriptor, float[] kernelWeights, float[] biasTerms, MPSCnnConvolutionFlags flags);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnFullyConnected -->
<div> <!-- start type MPSCnnKernel -->
<h3>New Type MetalPerformanceShaders.MPSCnnKernel</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnKernel : MetalPerformanceShaders.MPSKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnKernel (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnKernel (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLRegion ClipRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint DestinationFeatureChannelOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageEdgeMode EdgeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSOffset Offset { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSImage sourceImage, MPSImage destinationImage);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSRegion GetSourceRegion (Metal.MTLSize destinationSize);</span>
}
</pre>
</div> <!-- end type MPSCnnKernel -->
<div> <!-- start type MPSCnnLocalContrastNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnLocalContrastNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLocalContrastNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLocalContrastNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLocalContrastNormalization (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float P0 { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Pm { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Ps { get; set; }</span>
}
</pre>
</div> <!-- end type MPSCnnLocalContrastNormalization -->
<div> <!-- start type MPSCnnLogSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnLogSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnLogSoftMax : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnLogSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnLogSoftMax (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnLogSoftMax -->
<div> <!-- start type MPSCnnNeuron -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuron</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MPSCnnNeuron : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuron (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuron (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuron -->
<div> <!-- start type MPSCnnNeuronAbsolute -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronAbsolute</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronAbsolute : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsolute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronAbsolute (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronAbsolute (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronAbsolute -->
<div> <!-- start type MPSCnnNeuronLinear -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronLinear</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronLinear : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinear (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronLinear (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronLinear (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronLinear -->
<div> <!-- start type MPSCnnNeuronReLU -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronReLU</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronReLU : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLU (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronReLU (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronReLU (Metal.IMTLDevice device, float a);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronReLU -->
<div> <!-- start type MPSCnnNeuronSigmoid -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronSigmoid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronSigmoid : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronSigmoid (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronSigmoid (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronSigmoid -->
<div> <!-- start type MPSCnnNeuronTanH -->
<h3>New Type MetalPerformanceShaders.MPSCnnNeuronTanH</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnNeuronTanH : MetalPerformanceShaders.MPSCnnNeuron, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanH (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnNeuronTanH (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnNeuronTanH (Metal.IMTLDevice device, float a, float b);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float A { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float B { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnNeuronTanH -->
<div> <!-- start type MPSCnnPooling -->
<h3>New Type MetalPerformanceShaders.MPSCnnPooling</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPooling : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPooling (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPooling (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPooling (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsX { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint StrideInPixelsY { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPooling -->
<div> <!-- start type MPSCnnPoolingAverage -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingAverage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingAverage : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingAverage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingAverage (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingAverage -->
<div> <!-- start type MPSCnnPoolingMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnPoolingMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnPoolingMax : MetalPerformanceShaders.MPSCnnPooling, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnPoolingMax (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnPoolingMax (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, uint strideInPixelsX, uint strideInPixelsY);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnPoolingMax -->
<div> <!-- start type MPSCnnSoftMax -->
<h3>New Type MetalPerformanceShaders.MPSCnnSoftMax</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSoftMax : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMax (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSoftMax (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSoftMax (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnSoftMax -->
<div> <!-- start type MPSCnnSpatialNormalization -->
<h3>New Type MetalPerformanceShaders.MPSCnnSpatialNormalization</h3>
<pre class='added' data-is-non-breaking="">
public class MPSCnnSpatialNormalization : MetalPerformanceShaders.MPSCnnKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalization (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSCnnSpatialNormalization (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSCnnSpatialNormalization (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Alpha { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Beta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float Delta { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSCnnSpatialNormalization -->
<div> <!-- start type MPSDataType -->
<h3>New Type MetalPerformanceShaders.MPSDataType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSDataType {
	<span class='added added-field ' data-is-non-breaking="">Float32 = 268435488,</span>
	<span class='added added-field ' data-is-non-breaking="">FloatBit = 268435456,</span>
}
</pre>
</div> <!-- end type MPSDataType -->
<div> <!-- start type MPSImage -->
<h3>New Type MetalPerformanceShaders.MPSImage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImage : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImage (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImage (Metal.IMTLDevice device, MPSImageDescriptor imageDescriptor);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImage (Metal.IMTLTexture texture, uint featureChannels);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FeatureChannels { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Height { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Label { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfImages { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLPixelFormat PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Precision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLTexture Texture { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureType TextureType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureUsage Usage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Width { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual MPSPurgeableState SetPurgeableState (MPSPurgeableState state);</span>
}
</pre>
</div> <!-- end type MPSImage -->
<div> <!-- start type MPSImageConversion -->
<h3>New Type MetalPerformanceShaders.MPSImageConversion</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageConversion : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConversion (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageConversion (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageConversion (Metal.IMTLDevice device, MPSAlphaType srcAlpha, MPSAlphaType destAlpha, nfloat[] backgroundColor, CoreGraphics.CGColorConversionInfo conversionInfo);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSAlphaType DestinationAlpha { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSAlphaType SourceAlpha { get; }</span>
}
</pre>
</div> <!-- end type MPSImageConversion -->
<div> <!-- start type MPSImageDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSImageDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSImageFeatureChannelFormat ChannelFormat { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLCpuCacheMode CpuCacheMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FeatureChannels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Height { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfImages { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLPixelFormat PixelFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLStorageMode StorageMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLTextureUsage Usage { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Width { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetImageDescriptor (MPSImageFeatureChannelFormat channelFormat, uint width, uint height, uint featureChannels);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSImageDescriptor GetImageDescriptor (MPSImageFeatureChannelFormat channelFormat, uint width, uint height, uint featureChannels, uint numberOfImages, Metal.MTLTextureUsage usage);</span>
}
</pre>
</div> <!-- end type MPSImageDescriptor -->
<div> <!-- start type MPSImageFeatureChannelFormat -->
<h3>New Type MetalPerformanceShaders.MPSImageFeatureChannelFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MPSImageFeatureChannelFormat {
	<span class='added added-field ' data-is-non-breaking="">Float16 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Float32 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Invalid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm16 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unorm8 = 1,</span>
}
</pre>
</div> <!-- end type MPSImageFeatureChannelFormat -->
<div> <!-- start type MPSImageGaussianPyramid -->
<h3>New Type MetalPerformanceShaders.MPSImageGaussianPyramid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageGaussianPyramid : MetalPerformanceShaders.MPSImagePyramid, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianPyramid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageGaussianPyramid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageGaussianPyramid (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] kernelWeights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageGaussianPyramid -->
<div> <!-- start type MPSImageLaplacian -->
<h3>New Type MetalPerformanceShaders.MPSImageLaplacian</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImageLaplacian : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLaplacian (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImageLaplacian (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImageLaplacian (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float Bias { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type MPSImageLaplacian -->
<div> <!-- start type MPSImagePyramid -->
<h3>New Type MetalPerformanceShaders.MPSImagePyramid</h3>
<pre class='added' data-is-non-breaking="">
public class MPSImagePyramid : MetalPerformanceShaders.MPSUnaryImageKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImagePyramid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSImagePyramid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device, float centerWeight);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSImagePyramid (Metal.IMTLDevice device, uint kernelWidth, uint kernelHeight, float[] kernelWeights);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint KernelWidth { get; }</span>
}
</pre>
</div> <!-- end type MPSImagePyramid -->
<div> <!-- start type MPSMatrix -->
<h3>New Type MetalPerformanceShaders.MPSMatrix</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrix : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrix (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrix (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrix (Metal.IMTLBuffer buffer, MPSMatrixDescriptor descriptor);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLBuffer Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.IMTLDevice Device { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RowBytes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; }</span>
}
</pre>
</div> <!-- end type MPSMatrix -->
<div> <!-- start type MPSMatrixDescriptor -->
<h3>New Type MetalPerformanceShaders.MPSMatrixDescriptor</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixDescriptor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDescriptor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixDescriptor (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Columns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MPSDataType DataType { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint RowBytes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint Rows { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSMatrixDescriptor Create (uint rows, uint columns, uint rowBytes, MPSDataType dataType);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint GetRowBytes (uint columns, MPSDataType dataType);</span>
}
</pre>
</div> <!-- end type MPSMatrixDescriptor -->
<div> <!-- start type MPSMatrixMultiplication -->
<h3>New Type MetalPerformanceShaders.MPSMatrixMultiplication</h3>
<pre class='added' data-is-non-breaking="">
public class MPSMatrixMultiplication : MetalPerformanceShaders.MPSKernel, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixMultiplication (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSMatrixMultiplication (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MPSMatrixMultiplication (Metal.IMTLDevice device, bool transposeLeft, bool transposeRight, uint resultRows, uint resultColumns, uint interiorColumns, double alpha, double beta);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin LeftMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin ResultMatrixOrigin { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Metal.MTLOrigin RightMatrixOrigin { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeToCommandBuffer (Metal.IMTLCommandBuffer commandBuffer, MPSMatrix leftMatrix, MPSMatrix rightMatrix, MPSMatrix resultMatrix);</span>
}
</pre>
</div> <!-- end type MPSMatrixMultiplication -->
<div> <!-- start type MPSPurgeableState -->
<h3>New Type MetalPerformanceShaders.MPSPurgeableState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum MPSPurgeableState {
	<span class='added added-field ' data-is-non-breaking="">AllocationDeferred = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Empty = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">KeepCurrent = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NonVolatile = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Volatile = 3,</span>
}
</pre>
</div> <!-- end type MPSPurgeableState -->
<div> <!-- start type MPSTemporaryImage -->
<h3>New Type MetalPerformanceShaders.MPSTemporaryImage</h3>
<pre class='added' data-is-non-breaking="">
public class MPSTemporaryImage : MetalPerformanceShaders.MPSImage, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryImage (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MPSTemporaryImage (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReadCount { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryImage GetTemporaryImage (Metal.IMTLCommandBuffer commandBuffer, Metal.MTLTextureDescriptor textureDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static MPSTemporaryImage GetTemporaryImage (Metal.IMTLCommandBuffer commandBuffer, MPSImageDescriptor imageDescriptor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void PrefetchStorage (Metal.IMTLCommandBuffer commandBuffer, MPSImageDescriptor[] descriptorList);</span>
}
</pre>
</div> <!-- end type MPSTemporaryImage -->

</div> <!-- end namespace MetalPerformanceShaders -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLAsset --> <div>
<h3>Type Changed: ModelIO.MDLAsset</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLAsset FromScene (SceneKit.SCNScene scene, IMDLMeshBufferAllocator bufferAllocator);</span>
</pre>
</div>

</div> <!-- end type MDLAsset -->
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh FromGeometry (SceneKit.SCNGeometry geometry, IMDLMeshBufferAllocator bufferAllocator);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->
<!-- start type MDLObject --> <div>
<h3>Type Changed: ModelIO.MDLObject</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLObject FromNode (SceneKit.SCNNode node, IMDLMeshBufferAllocator bufferAllocator);</span>
</pre>
</div>

</div> <!-- end type MDLObject -->
<!-- start type MDLSubmesh --> <div>
<h3>Type Changed: ModelIO.MDLSubmesh</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLSubmesh FromGeometryElement (SceneKit.SCNGeometryElement element, IMDLMeshBufferAllocator bufferAllocator);</span>
</pre>
</div>

</div> <!-- end type MDLSubmesh -->
<!-- start type MDLTransform --> <div>
<h3>Type Changed: ModelIO.MDLTransform</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSCopying</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
</pre>
</div>

</div> <!-- end type MDLTransform -->
<!-- start type MDLVertexDescriptor --> <div>
<h3>Type Changed: ModelIO.MDLVertexDescriptor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLVertexDescriptor FromMetal (Metal.MTLVertexDescriptor descriptor, out Foundation.NSError error);</span>
</pre>
</div>

</div> <!-- end type MDLVertexDescriptor -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string SdkVersion = <span class='removed removed-inline removed-breaking-inline'>"9.2"</span> <span class='added '>"10.0"</span>;
</div><div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"9.8.2"</span> <span class='added '>"9.99.3"</span>;
</div></pre>
<div>
<p>Added fields:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public static const string ExternalAccessoryLibrary = "/System/Library/Frameworks/ExternalAccessory.framework/ExternalAccessory";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string HomeKitLibrary = "/System/Library/Frameworks/HomeKit.framework/HomeKit";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string MultipeerConnectivityLibrary = "/System/Library/Frameworks/MultipeerConnectivity.framework/MultipeerConnectivity";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string PhotosLibrary = "/System/Library/Frameworks/Photos.framework/Photos";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string ReplayKitLibrary = "/System/Library/Frameworks/ReplayKit.framework/ReplayKit";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string UserNotificationsLibrary = "/System/Library/Frameworks/UserNotifications.framework/UserNotifications";</span>
	<span class='added added-field ' data-is-non-breaking="">public static const string VideoSubscriberAccountLibrary = "/System/Library/Frameworks/VideoSubscriberAccount.framework/VideoSubscriberAccount";</span>
</pre>
</div>

</div> <!-- end type Constants -->
<!-- start type Runtime --> <div>
<h3>Type Changed: ObjCRuntime.Runtime</h3>
<div>
<p>Added events:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event MarshalManagedExceptionHandler MarshalManagedException;</span>
	<span class='added added-event ' data-is-non-breaking="">public event MarshalObjectiveCExceptionHandler MarshalObjectiveCException;</span>
</pre>
</div>

</div> <!-- end type Runtime -->
<div> <!-- start type MarshalManagedExceptionEventArgs -->
<h3>New Type ObjCRuntime.MarshalManagedExceptionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class MarshalManagedExceptionEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalManagedExceptionEventArgs ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Exception Exception { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MarshalManagedExceptionMode ExceptionMode { get; set; }</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionEventArgs -->
<div> <!-- start type MarshalManagedExceptionHandler -->
<h3>New Type ObjCRuntime.MarshalManagedExceptionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MarshalManagedExceptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalManagedExceptionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, MarshalManagedExceptionEventArgs args, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, MarshalManagedExceptionEventArgs args);</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionHandler -->
<div> <!-- start type MarshalManagedExceptionMode -->
<h3>New Type ObjCRuntime.MarshalManagedExceptionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MarshalManagedExceptionMode {
	<span class='added added-field ' data-is-non-breaking="">Abort = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ThrowObjectiveCException = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UnwindNativeCode = 1,</span>
}
</pre>
</div> <!-- end type MarshalManagedExceptionMode -->
<div> <!-- start type MarshalObjectiveCExceptionEventArgs -->
<h3>New Type ObjCRuntime.MarshalObjectiveCExceptionEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class MarshalObjectiveCExceptionEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalObjectiveCExceptionEventArgs ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSException Exception { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public MarshalObjectiveCExceptionMode ExceptionMode { get; set; }</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionEventArgs -->
<div> <!-- start type MarshalObjectiveCExceptionHandler -->
<h3>New Type ObjCRuntime.MarshalObjectiveCExceptionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MarshalObjectiveCExceptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MarshalObjectiveCExceptionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, MarshalObjectiveCExceptionEventArgs args, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, MarshalObjectiveCExceptionEventArgs args);</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionHandler -->
<div> <!-- start type MarshalObjectiveCExceptionMode -->
<h3>New Type ObjCRuntime.MarshalObjectiveCExceptionMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MarshalObjectiveCExceptionMode {
	<span class='added added-field ' data-is-non-breaking="">Abort = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Disable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ThrowManagedException = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UnwindManagedCode = 1,</span>
}
</pre>
</div> <!-- end type MarshalObjectiveCExceptionMode -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace OpenGLES --> <div> 
<h2>Namespace OpenGLES</h2>
<!-- start type EAGLContext --> <div>
<h3>Type Changed: OpenGLES.EAGLContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PresentRenderBuffer (uint target, double presentationTime);</span>
</pre>
</div>

</div> <!-- end type EAGLContext -->

</div> <!-- end namespace OpenGLES -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNAnimatable --> <div>
<h3>Type Changed: SceneKit.SCNAnimatable</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNAnimatable -->
<!-- start type SCNCamera --> <div>
<h3>Type Changed: SceneKit.SCNCamera</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat AverageGray { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BloomBlurRadius { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BloomIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat BloomThreshold { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ColorFringeIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ColorFringeStrength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty ColorGrading { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Contrast { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ExposureAdaptationBrighteningSpeedFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ExposureAdaptationDarkeningSpeedFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ExposureOffset { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MaximumExposure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MinimumExposure { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat MotionBlurIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Saturation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat VignettingIntensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat VignettingPower { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsExposureAdaptation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsHdr { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat WhitePoint { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNCamera -->
<!-- start type SCNConstraint --> <div>
<h3>Type Changed: SceneKit.SCNConstraint</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNConstraint -->
<!-- start type SCNFloor --> <div>
<h3>Type Changed: SceneKit.SCNFloor</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Length { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ReflectionCategoryBitMask { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Width { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNFloor -->
<!-- start type SCNGeometry --> <div>
<h3>Type Changed: SceneKit.SCNGeometry</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNGeometry -->
<!-- start type SCNGeometryPrimitiveType --> <div>
<h3>Type Changed: SceneKit.SCNGeometryPrimitiveType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Polygon = 4,</span>
</pre>
</div>

</div> <!-- end type SCNGeometryPrimitiveType -->
<!-- start type SCNGeometrySourceSemantic --> <div>
<h3>Type Changed: SceneKit.SCNGeometrySourceSemantic</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Tangent { get; }</span>
</pre>
</div>

</div> <!-- end type SCNGeometrySourceSemantic -->
<!-- start type SCNHitTest --> <div>
<h3>Type Changed: SceneKit.SCNHitTest</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionCategoryBitMaskKey { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTest -->
<!-- start type SCNHitTestResult --> <div>
<h3>Type Changed: SceneKit.SCNHitTestResult</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNNode BoneNode { get; }</span>
</pre>
</div>

</div> <!-- end type SCNHitTestResult -->
<!-- start type SCNLight --> <div>
<h3>Type Changed: SceneKit.SCNLight</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl IesProfileUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Intensity { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Temperature { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNLight -->
<!-- start type SCNLightType --> <div>
<h3>Type Changed: SceneKit.SCNLightType</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Ies { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Probe { get; }</span>
</pre>
</div>

</div> <!-- end type SCNLightType -->
<!-- start type SCNLightingModel --> <div>
<h3>Type Changed: SceneKit.SCNLightingModel</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PhysicallyBased { get; }</span>
</pre>
</div>

</div> <!-- end type SCNLightingModel -->
<!-- start type SCNLookAtConstraint --> <div>
<h3>Type Changed: SceneKit.SCNLookAtConstraint</h3>
<p>Modified properties:</p>
<pre>
<div data-is-non-breaking="">	public virtual SCNNode Target { get; <span class='added '>set;</span> }
</div></pre>

</div> <!-- end type SCNLookAtConstraint -->
<!-- start type SCNMaterial --> <div>
<h3>Type Changed: SceneKit.SCNMaterial</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty Metalness { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty Roughness { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNMaterial -->
<!-- start type SCNMaterialProperty --> <div>
<h3>Type Changed: SceneKit.SCNMaterialProperty</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSObject BorderColor { get; set; }</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNMaterialProperty -->
<!-- start type SCNMorpher --> <div>
<h3>Type Changed: SceneKit.SCNMorpher</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNMorpher -->
<!-- start type SCNNode --> <div>
<h3>Type Changed: SceneKit.SCNNode</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMovabilityHint MovabilityHint { get; set; }</span>
</pre>
</div>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use the overload that takes a SCNNodeHandler instead")]
	public virtual void EnumerateChildNodes (SCNNodePredicate predicate);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateChildNodes (SCNNodeHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateHierarchy (SCNNodeHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNNode -->
<!-- start type SCNParticleProperty --> <div>
<h3>Type Changed: SceneKit.SCNParticleProperty</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContactNormal { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ContactPoint { get; }</span>
</pre>
</div>

</div> <!-- end type SCNParticleProperty -->
<!-- start type SCNParticleSystem --> <div>
<h3>Type Changed: SceneKit.SCNParticleSystem</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNParticleSystem -->
<!-- start type SCNPhysicsShapeOptionsKeys --> <div>
<h3>Type Changed: SceneKit.SCNPhysicsShapeOptionsKeys</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CollisionMargin { get; }</span>
</pre>
</div>

</div> <!-- end type SCNPhysicsShapeOptionsKeys -->
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void Render ();</span>
</pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIKit.UIImage GetSnapshot (double time, CoreGraphics.CGSize size, SCNAntialiasingMode antialiasingMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Update (SCNNode[] lightProbes, double time);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNScene --> <div>
<h3>Type Changed: SceneKit.SCNScene</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SCNMaterialProperty LightingEnvironment { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool WriteToUrl (Foundation.NSUrl url, Foundation.NSDictionary options, ISCNSceneExportDelegate aDelegate, SCNSceneExportProgressHandler exportProgressHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public bool WriteToUrl (Foundation.NSUrl url, SCNSceneLoadingOptions options, ISCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);</span>
</pre>
</div>

</div> <!-- end type SCNScene -->
<!-- start type SCNSceneLoadingOptions --> <div>
<h3>Type Changed: SceneKit.SCNSceneLoadingOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool? PreserveOriginalTopology { get; set; }</span>
</pre>
</div>

</div> <!-- end type SCNSceneLoadingOptions -->
<!-- start type SCNSceneSourceLoading --> <div>
<h3>Type Changed: SceneKit.SCNSceneSourceLoading</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OptionPreserveOriginalTopology { get; }</span>
</pre>
</div>

</div> <!-- end type SCNSceneSourceLoading -->
<!-- start type SCNSceneSourceProperties --> <div>
<h3>Type Changed: SceneKit.SCNSceneSourceProperties</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetAuthorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetAuthoringToolKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetUnitMeterKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssetUnitNameKey { get; }</span>
</pre>
</div>

</div> <!-- end type SCNSceneSourceProperties -->
<!-- start type SCNTechnique --> <div>
<h3>Type Changed: SceneKit.SCNTechnique</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetSpeed (nfloat speed, Foundation.NSString key);</span>
</pre>
</div>

</div> <!-- end type SCNTechnique -->
<div> <!-- start type ISCNSceneExportDelegate -->
<h3>New Type SceneKit.ISCNSceneExportDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ISCNSceneExportDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISCNSceneExportDelegate -->
<div> <!-- start type SCNAnimatable_Extensions -->
<h3>New Type SceneKit.SCNAnimatable_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SCNAnimatable_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void SetSpeed (ISCNAnimatable This, nfloat speed, Foundation.NSString key);</span>
}
</pre>
</div> <!-- end type SCNAnimatable_Extensions -->
<div> <!-- start type SCNMovabilityHint -->
<h3>New Type SceneKit.SCNMovabilityHint</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SCNMovabilityHint {
	<span class='added added-field ' data-is-non-breaking="">Fixed = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Movable = 1,</span>
}
</pre>
</div> <!-- end type SCNMovabilityHint -->
<div> <!-- start type SCNNodeHandler -->
<h3>New Type SceneKit.SCNNodeHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate SCNNodeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNNodeHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (SCNNode node, out bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (out bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (SCNNode node, out bool stop);</span>
}
</pre>
</div> <!-- end type SCNNodeHandler -->
<div> <!-- start type SCNSceneExportDelegate -->
<h3>New Type SceneKit.SCNSceneExportDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class SCNSceneExportDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, ISCNSceneExportDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNSceneExportDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNSceneExportDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SCNSceneExportDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSUrl WriteImage (UIKit.UIImage image, Foundation.NSUrl documentUrl, Foundation.NSUrl originalImageUrl);</span>
}
</pre>
</div> <!-- end type SCNSceneExportDelegate -->
<div> <!-- start type SCNSceneExportDelegate_Extensions -->
<h3>New Type SceneKit.SCNSceneExportDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SCNSceneExportDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSUrl WriteImage (ISCNSceneExportDelegate This, UIKit.UIImage image, Foundation.NSUrl documentUrl, Foundation.NSUrl originalImageUrl);</span>
}
</pre>
</div> <!-- end type SCNSceneExportDelegate_Extensions -->
<div> <!-- start type SCNSceneExportProgressHandler -->
<h3>New Type SceneKit.SCNSceneExportProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate SCNSceneExportProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SCNSceneExportProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (float totalProgress, Foundation.NSError error, out bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (out bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (float totalProgress, Foundation.NSError error, out bool stop);</span>
}
</pre>
</div> <!-- end type SCNSceneExportProgressHandler -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace Security --> <div> 
<h2>Namespace Security</h2>
<!-- start type SslContext --> <div>
<h3>Type Changed: Security.SslContext</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("SetSessionStrengthPolicy is not available anymore.")]
	public SslStatus SetSessionStrengthPolicy (SslSessionStrengthPolicy policyStrength);</span>
</div></pre>

</div> <!-- end type SslContext -->

</div> <!-- end namespace Security -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SK3DNode --> <div>
<h3>Type Changed: SpriteKit.SK3DNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SK3DNode -->
<!-- start type SKAction --> <div>
<h3>Type Changed: SpriteKit.SKAction</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction Animate (SKWarpGeometry[] warps, Foundation.NSNumber[] times);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction Animate (SKWarpGeometry[] warps, Foundation.NSNumber[] times, bool restore);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction ScaleTo (CoreGraphics.CGSize size, double sec);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAction WarpTo (SKWarpGeometry warp, double duration);</span>
</pre>
</div>

</div> <!-- end type SKAction -->
<!-- start type SKAudioNode --> <div>
<h3>Type Changed: SpriteKit.SKAudioNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKAudioNode -->
<!-- start type SKCameraNode --> <div>
<h3>Type Changed: SpriteKit.SKCameraNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKCameraNode -->
<!-- start type SKCropNode --> <div>
<h3>Type Changed: SpriteKit.SKCropNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKCropNode -->
<!-- start type SKEffectNode --> <div>
<h3>Type Changed: SpriteKit.SKEffectNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ISKWarpable</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SubdivisionLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKWarpGeometry WarpGeometry { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type SKEffectNode -->
<!-- start type SKEmitterNode --> <div>
<h3>Type Changed: SpriteKit.SKEmitterNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKEmitterNode -->
<!-- start type SKFieldNode --> <div>
<h3>Type Changed: SpriteKit.SKFieldNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKFieldNode -->
<!-- start type SKLabelNode --> <div>
<h3>Type Changed: SpriteKit.SKLabelNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKLabelNode -->
<!-- start type SKLightNode --> <div>
<h3>Type Changed: SpriteKit.SKLightNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKLightNode -->
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanBecomeFocused { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.IUIFocusEnvironment[] PreferredFocusEnvironments { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIView PreferredFocusedView { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateFocus (UIKit.UIFocusUpdateContext context, UIKit.UIFocusAnimationCoordinator coordinator);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetNeedsFocusUpdate ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldUpdateFocus (UIKit.UIFocusUpdateContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateFocusIfNeeded ();</span>
</pre>
</div>

</div> <!-- end type SKNode -->
<!-- start type SKReferenceNode --> <div>
<h3>Type Changed: SpriteKit.SKReferenceNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKReferenceNode -->
<!-- start type SKScene --> <div>
<h3>Type Changed: SpriteKit.SKScene</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ISKWarpable</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SceneDidLoad ();</span>
</pre>
</div>

</div> <!-- end type SKScene -->
<!-- start type SKShader --> <div>
<h3>Type Changed: SpriteKit.SKShader</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKAttribute[] Attributes { get; set; }</span>
</pre>
</div>

</div> <!-- end type SKShader -->
<!-- start type SKShapeNode --> <div>
<h3>Type Changed: SpriteKit.SKShapeNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>

</div> <!-- end type SKShapeNode -->
<!-- start type SKSpriteNode --> <div>
<h3>Type Changed: SpriteKit.SKSpriteNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">ISKWarpable</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SubdivisionLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKWarpGeometry WarpGeometry { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ScaleTo (CoreGraphics.CGSize size);</span>
</pre>
</div>

</div> <!-- end type SKSpriteNode -->
<!-- start type SKVideoNode --> <div>
<h3>Type Changed: SpriteKit.SKVideoNode</h3>
<div>
<p>Added interfaces:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusEnvironment</span>
	<span class='added added-interface ' data-is-non-breaking="">UIKit.IUIFocusItem</span>
</pre>
</div>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public SKVideoNode FromUrl (Foundation.NSUrl <span class='removed removed-inline '>videoURL</span> <span class='added '>videoUrl</span>)
</div></pre>

</div> <!-- end type SKVideoNode -->
<!-- start type SKView --> <div>
<h3>Type Changed: SpriteKit.SKView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual ISKViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint PreferredFramesPerSecond { get; set; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
</pre>
</div>

</div> <!-- end type SKView -->
<div> <!-- start type ISKViewDelegate -->
<h3>New Type SpriteKit.ISKViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface ISKViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type ISKViewDelegate -->
<div> <!-- start type ISKWarpable -->
<h3>New Type SpriteKit.ISKWarpable</h3>
<pre class='added' data-is-non-breaking="">
public interface ISKWarpable : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nint SubdivisionLevels { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKWarpGeometry WarpGeometry { get; set; }</span>
}
</pre>
</div> <!-- end type ISKWarpable -->
<div> <!-- start type SKAttribute -->
<h3>New Type SpriteKit.SKAttribute</h3>
<pre class='added' data-is-non-breaking="">
public class SKAttribute : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttribute (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttribute (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttribute (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttribute (string name, SKAttributeType type);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKAttributeType Type { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SKAttribute Create (string name, SKAttributeType type);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKAttribute -->
<div> <!-- start type SKAttributeType -->
<h3>New Type SpriteKit.SKAttributeType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKAttributeType {
	<span class='added added-field ' data-is-non-breaking="">Float = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HalfFloat = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorFloat2 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorFloat3 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorFloat4 = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorHalfFloat2 = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorHalfFloat3 = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">VectorHalfFloat4 = 8,</span>
}
</pre>
</div> <!-- end type SKAttributeType -->
<div> <!-- start type SKAttributeValue -->
<h3>New Type SpriteKit.SKAttributeValue</h3>
<pre class='added' data-is-non-breaking="">
public class SKAttributeValue : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttributeValue ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKAttributeValue (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttributeValue (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKAttributeValue (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual float FloatValue { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector2 VectorFloat2Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector3 VectorFloat3Value { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual OpenTK.Vector4 VectorFloat4Value { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (OpenTK.Vector2 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (OpenTK.Vector3 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (OpenTK.Vector4 value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKAttributeValue Create (float value);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKAttributeValue -->
<div> <!-- start type SKTileAdjacencyMask -->
<h3>New Type SpriteKit.SKTileAdjacencyMask</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKTileAdjacencyMask {
	<span class='added added-field ' data-is-non-breaking="">All = 255,</span>
	<span class='added added-field ' data-is-non-breaking="">Down = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">DownEdge = 199,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatAll = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatDown = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatLowerLeft = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatLowerRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatUp = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatUpperLeft = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">HexFlatUpperRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyAll = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyLeft = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyLowerLeft = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyLowerRight = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyRight = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyUpperLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">HexPointyUpperRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Left = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">LeftEdge = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerLeft = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerLeftCorner = 253,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerLeftEdge = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerRight = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerRightCorner = 127,</span>
	<span class='added added-field ' data-is-non-breaking="">LowerRightEdge = 193,</span>
	<span class='added added-field ' data-is-non-breaking="">Right = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">RightEdge = 241,</span>
	<span class='added added-field ' data-is-non-breaking="">Up = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UpEdge = 124,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperLeft = 128,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperLeftCorner = 247,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperLeftEdge = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperRight = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperRightCorner = 223,</span>
	<span class='added added-field ' data-is-non-breaking="">UpperRightEdge = 112,</span>
}
</pre>
</div> <!-- end type SKTileAdjacencyMask -->
<div> <!-- start type SKTileDefinition -->
<h3>New Type SpriteKit.SKTileDefinition</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileDefinition : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileDefinition (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture texture);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileDefinition (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture texture, CoreGraphics.CGSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture texture, SKTexture normalTexture, CoreGraphics.CGSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture[] textures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileDefinition (SKTexture[] textures, SKTexture[] normalTextures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipHorizontally { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool FlipVertically { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTexture[] NormalTextures { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PlacementWeight { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileDefinitionRotation Rotation { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize Size { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTexture[] Textures { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat TimePerFrame { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSMutableDictionary UserData { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture texture);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture texture, CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture texture, SKTexture normalTexture, CoreGraphics.CGSize size);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture[] textures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileDefinition Create (SKTexture[] textures, SKTexture[] normalTextures, CoreGraphics.CGSize size, nfloat timePerFrame);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKTileDefinition -->
<div> <!-- start type SKTileDefinitionRotation -->
<h3>New Type SpriteKit.SKTileDefinitionRotation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKTileDefinitionRotation {
	<span class='added added-field ' data-is-non-breaking="">Angle0 = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Angle180 = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Angle270 = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Angle90 = 1,</span>
}
</pre>
</div> <!-- end type SKTileDefinitionRotation -->
<div> <!-- start type SKTileGroup -->
<h3>New Type SpriteKit.SKTileGroup</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileGroup : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup (SKTileDefinition tileDefinition);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroup (SKTileGroupRule[] rules);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileGroupRule[] Rules { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroup Create (SKTileDefinition tileDefinition);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroup Create (SKTileGroupRule[] rules);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroup CreateEmpty ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKTileGroup -->
<div> <!-- start type SKTileGroupRule -->
<h3>New Type SpriteKit.SKTileGroupRule</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileGroupRule : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroupRule ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroupRule (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroupRule (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileGroupRule (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileGroupRule (SKTileAdjacencyMask adjacency, SKTileDefinition[] tileDefinitions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileAdjacencyMask Adjacency { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileDefinition[] TileDefinitions { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileGroupRule Create (SKTileAdjacencyMask adjacency, SKTileDefinition[] tileDefinitions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKTileGroupRule -->
<div> <!-- start type SKTileMapNode -->
<h3>New Type SpriteKit.SKTileMapNode</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileMapNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;SKNode&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIFocusEnvironment, UIKit.IUIFocusItem {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileMapNode (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileMapNode (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup tileGroup);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileMapNode (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup[] tileGroupLayout);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint AnchorPoint { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKBlendMode BlendMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIColor Color { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat ColorBlendFactor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool EnableAutomapping { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint LightingBitMask { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize MapSize { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfColumns { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint NumberOfRows { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKShader Shader { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileSet TileSet { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize TileSize { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileMapNode Create (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileMapNode Create (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup tileGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileMapNode Create (SKTileSet tileSet, uint columns, uint rows, CoreGraphics.CGSize tileSize, SKTileGroup[] tileGroupLayout);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Fill (SKTileGroup tileGroup);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint GetCenterOfTile (uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetTileColumnIndex (CoreGraphics.CGPoint position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKTileDefinition GetTileDefinition (uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual SKTileGroup GetTileGroup (uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint GetTileRowIndex (CoreGraphics.CGPoint position);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTileGroup (SKTileGroup tileGroup, uint column, uint row);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetTileGroup (SKTileGroup tileGroup, SKTileDefinition tileDefinition, uint column, uint row);</span>
}
</pre>
</div> <!-- end type SKTileMapNode -->
<div> <!-- start type SKTileSet -->
<h3>New Type SpriteKit.SKTileSet</h3>
<pre class='added' data-is-non-breaking="">
public class SKTileSet : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileSet (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet (SKTileGroup[] tileGroups);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKTileSet (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKTileSet (SKTileGroup[] tileGroups, SKTileSetType tileSetType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileGroup DefaultTileGroup { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize DefaultTileSize { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileGroup[] TileGroups { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual SKTileSetType Type { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet Create (SKTileGroup[] tileGroups);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet Create (SKTileGroup[] tileGroups, SKTileSetType tileSetType);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet FromName (string name);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKTileSet FromUrl (Foundation.NSUrl url);</span>
}
</pre>
</div> <!-- end type SKTileSet -->
<div> <!-- start type SKTileSetType -->
<h3>New Type SpriteKit.SKTileSetType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SKTileSetType {
	<span class='added added-field ' data-is-non-breaking="">Grid = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">HexagonalFlat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HexagonalPointy = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Isometric = 1,</span>
}
</pre>
</div> <!-- end type SKTileSetType -->
<div> <!-- start type SKViewDelegate -->
<h3>New Type SpriteKit.SKViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class SKViewDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, ISKViewDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldRender (SKView view, double time);</span>
}
</pre>
</div> <!-- end type SKViewDelegate -->
<div> <!-- start type SKViewDelegate_Extensions -->
<h3>New Type SpriteKit.SKViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class SKViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldRender (ISKViewDelegate This, SKView view, double time);</span>
}
</pre>
</div> <!-- end type SKViewDelegate_Extensions -->
<div> <!-- start type SKWarpGeometry -->
<h3>New Type SpriteKit.SKWarpGeometry</h3>
<pre class='added' data-is-non-breaking="">
public class SKWarpGeometry : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometry ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometry (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometry (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometry (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type SKWarpGeometry -->
<div> <!-- start type SKWarpGeometryGrid -->
<h3>New Type SpriteKit.SKWarpGeometryGrid</h3>
<pre class='added' data-is-non-breaking="">
public class SKWarpGeometryGrid : SpriteKit.SKWarpGeometry, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometryGrid (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometryGrid (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected SKWarpGeometryGrid (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SKWarpGeometryGrid (nint cols, nint rows, OpenTK.Vector2[] sourcePositions, OpenTK.Vector2[] destPositions);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfColumns { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint NumberOfRows { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint VertexCount { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static SKWarpGeometryGrid Create (nint cols, nint rows);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKWarpGeometryGrid Create (nint cols, nint rows, OpenTK.Vector2[] sourcePositions, OpenTK.Vector2[] destPositions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetDestPosition (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public static SKWarpGeometryGrid GetGrid ();</span>
	<span class='added added-method ' data-is-non-breaking="">public SKWarpGeometryGrid GetGridByReplacingDestPositions (OpenTK.Vector2[] destPositions);</span>
	<span class='added added-method ' data-is-non-breaking="">public SKWarpGeometryGrid GetGridByReplacingSourcePositions (OpenTK.Vector2[] sourcePositions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual OpenTK.Vector2 GetSourcePosition (nint index);</span>
}
</pre>
</div> <!-- end type SKWarpGeometryGrid -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace TVMLKit --> <div> 
<h2>Namespace TVMLKit</h2>
<!-- start type TVElementUpdateType --> <div>
<h3>Type Changed: TVMLKit.TVElementUpdateType</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Styles = 4,</span>
</pre>
</div>

</div> <!-- end type TVElementUpdateType -->
<!-- start type TVInterfaceCreating_Extensions --> <div>
<h3>Type Changed: TVMLKit.TVInterfaceCreating_Extensions</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static ObjCRuntime.Class GetCollectionViewCellClass (ITVInterfaceCreating This, TVViewElement element);</span>
</pre>
</div>

</div> <!-- end type TVInterfaceCreating_Extensions -->
<!-- start type TVInterfaceFactory --> <div>
<h3>Type Changed: TVMLKit.TVInterfaceFactory</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual ObjCRuntime.Class GetCollectionViewCellClass (TVViewElement element);</span>
</pre>
</div>

</div> <!-- end type TVInterfaceFactory -->
<!-- start type TVViewElementStyle --> <div>
<h3>Type Changed: TVMLKit.TVViewElementStyle</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIEdgeInsets FocusMargin { get; }</span>
</pre>
</div>

</div> <!-- end type TVViewElementStyle -->

</div> <!-- end namespace TVMLKit -->
<!-- start namespace UIKit --> <div> 
<h2>Namespace UIKit</h2>
<!-- start type NSLayoutConstraint --> <div>
<h3>Type Changed: UIKit.NSLayoutConstraint</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIKit.NSLayoutAnchor&lt;AnchorType&gt; FirstAnchor&lt;AnchorType&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public UIKit.NSLayoutAnchor&lt;AnchorType&gt; SecondAnchor&lt;AnchorType&gt; ();</span>
</pre>
</div>

</div> <!-- end type NSLayoutConstraint -->
<!-- start type NSTextTab --> <div>
<h3>Type Changed: UIKit.NSTextTab</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">Foundation.INSSecureCoding</span>
</pre>
</div>

</div> <!-- end type NSTextTab -->
<!-- start type UIAccessibility --> <div>
<h3>Type Changed: UIKit.UIAccessibility</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static bool IsAssistiveTouchRunning { get; }</span>
</pre>
</div>

</div> <!-- end type UIAccessibility -->
<!-- start type UIAccessibilityElement --> <div>
<h3>Type Changed: UIKit.UIAccessibilityElement</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect AccessibilityFrameInContainerSpace { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIAccessibilityElement -->
<!-- start type UIApplication --> <div>
<h3>Type Changed: UIKit.UIApplication</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void OpenUrl (Foundation.NSUrl url, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;bool&gt; completion);</span>
</pre>
</div>

</div> <!-- end type UIApplication -->
<!-- start type UIBarItem --> <div>
<h3>Type Changed: UIKit.UIBarItem</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssistiveTouchStatusDidChangeNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static long TraitTabBar { get; }</span>
</pre>
</div>
<!-- start type UIBarItem.Notifications --> <div>
<h3>Type Changed: UIKit.UIBarItem.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTouchStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIBarItem.Notifications -->

</div> <!-- end type UIBarItem -->
<!-- start type UIBlurEffectStyle --> <div>
<h3>Type Changed: UIKit.UIBlurEffectStyle</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">Prominent = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Regular = 4,</span>
</pre>
</div>

</div> <!-- end type UIBlurEffectStyle -->
<!-- start type UICollectionView --> <div>
<h3>Type Changed: UIKit.UICollectionView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUICollectionViewDataSourcePrefetching PrefetchDataSource { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefetchingEnabled { get; set; }</span>
</pre>
</div>

</div> <!-- end type UICollectionView -->
<!-- start type UICollectionViewFlowLayout --> <div>
<h3>Type Changed: UIKit.UICollectionViewFlowLayout</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGSize UICollectionViewFlowLayoutAutomaticSize { get; }</span>
</pre>
</div>

</div> <!-- end type UICollectionViewFlowLayout -->
<!-- start type UIColor --> <div>
<h3>Type Changed: UIKit.UIColor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIColor FromDisplayP3 (nfloat red, nfloat green, nfloat blue, nfloat alpha);</span>
</pre>
</div>

</div> <!-- end type UIColor -->
<!-- start type UIContentSizeCategory --> <div>
<h3>Type Changed: UIKit.UIContentSizeCategory</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AccessibilityExtraExtraExtraLarge = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessibilityExtraExtraLarge = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessibilityExtraLarge = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessibilityLarge = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessibilityMedium = 7,</span>
</pre>
</div>

</div> <!-- end type UIContentSizeCategory -->
<!-- start type UIFocusGuide --> <div>
<h3>Type Changed: UIKit.UIFocusGuide</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIFocusEnvironment[] PreferredFocusEnvironments { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIFocusGuide -->
<!-- start type UIFocusHeading --> <div>
<h3>Type Changed: UIKit.UIFocusHeading</h3>
<div>
<p>Added value:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
</pre>
</div>

</div> <!-- end type UIFocusHeading -->
<!-- start type UIFocusUpdateContext --> <div>
<h3>Type Changed: UIKit.UIFocusUpdateContext</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIFocusItem NextFocusedItem { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIFocusItem PreviouslyFocusedItem { get; }</span>
</pre>
</div>

</div> <!-- end type UIFocusUpdateContext -->
<!-- start type UIFont --> <div>
<h3>Type Changed: UIKit.UIFont</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFont GetPreferredFontForTextStyle (Foundation.NSString uiFontTextStyle, UITraitCollection traitCollection);</span>
</pre>
</div>

</div> <!-- end type UIFont -->
<!-- start type UIFontDescriptor --> <div>
<h3>Type Changed: UIKit.UIFontDescriptor</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UIFontDescriptor GetPreferredDescriptorForTextStyle (Foundation.NSString uiFontTextStyle, UITraitCollection traitCollection);</span>
</pre>
</div>

</div> <!-- end type UIFontDescriptor -->
<!-- start type UIImage --> <div>
<h3>Type Changed: UIKit.UIImage</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssistiveTouchStatusDidChangeNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIGraphicsImageRendererFormat ImageRendererFormat { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static long TraitTabBar { get; }</span>
</pre>
</div>
<!-- start type UIImage.Notifications --> <div>
<h3>Type Changed: UIKit.UIImage.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTouchStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIImage.Notifications -->

</div> <!-- end type UIImage -->
<!-- start type UIInputViewController --> <div>
<h3>Type Changed: UIKit.UIInputViewController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void HandleInputModeList (UIView fromView, UIEvent withEvent);</span>
</pre>
</div>

</div> <!-- end type UIInputViewController -->
<!-- start type UIKeyboardType --> <div>
<h3>Type Changed: UIKit.UIKeyboardType</h3>
<div>
<p>Added values:</p>
<pre class='added' data-is-non-breaking="">
	<span class='added added-field ' data-is-non-breaking="">AsciiCapable = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">AsciiCapableNumberPad = 11,</span>
</pre>
</div>

</div> <!-- end type UIKeyboardType -->
<!-- start type UILabel --> <div>
<h3>Type Changed: UIKit.UILabel</h3>
<div>
<p>Added interface:</p>
<pre>
	<span class='added added-interface ' data-is-non-breaking="">IUIContentSizeCategoryAdjusting</span>
</pre>
</div>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AdjustsFontForContentSizeCategory { get; set; }</span>
</pre>
</div>

</div> <!-- end type UILabel -->
<!-- start type UIPresentationController --> <div>
<h3>Type Changed: UIKit.UIPresentationController</h3>
<p>Obsoleted constructors:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-constructor' data-is-non-breaking="">[Obsolete ("Removed in iOS10. Use .ctor(UIViewController,UIViewController)")]
	public UIPresentationController ();</span>
</div></pre>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIFocusEnvironment[] PreferredFocusEnvironments { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIPresentationController -->
<!-- start type UIScreen --> <div>
<h3>Type Changed: UIKit.UIScreen</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIFocusItem FocusedItem { get; }</span>
</pre>
</div>

</div> <!-- end type UIScreen -->
<!-- start type UISearchBar --> <div>
<h3>Type Changed: UIKit.UISearchBar</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString TextContentType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UISearchBar -->
<!-- start type UITabBar --> <div>
<h3>Type Changed: UIKit.UITabBar</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIColor UnselectedItemTintColor { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITabBar -->
<!-- start type UITabBarItem --> <div>
<h3>Type Changed: UIKit.UITabBarItem</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIColor BadgeColor { get; set; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIStringAttributes GetBadgeTextAttributes (UIControlState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public void SetBadgeTextAttributes (UIStringAttributes textAttributes, UIControlState state);</span>
</pre>
</div>

</div> <!-- end type UITabBarItem -->
<!-- start type UITableView --> <div>
<h3>Type Changed: UIKit.UITableView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITableViewDataSourcePrefetching PrefetchDataSource { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITableView -->
<!-- start type UITextDocumentProxy --> <div>
<h3>Type Changed: UIKit.UITextDocumentProxy</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextInputMode DocumentInputMode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString TextContentType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextDocumentProxy -->
<!-- start type UITextField --> <div>
<h3>Type Changed: UIKit.UITextField</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString TextContentType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextField -->
<!-- start type UITextView --> <div>
<h3>Type Changed: UIKit.UITextView</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString TextContentType { get; set; }</span>
</pre>
</div>

</div> <!-- end type UITextView -->
<!-- start type UITraitCollection --> <div>
<h3>Type Changed: UIKit.UITraitCollection</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIDisplayGamut DisplayGamut { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITraitEnvironmentLayoutDirection LayoutDirection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string PreferredContentSizeCategory { get; }</span>
</pre>
</div>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static UITraitCollection FromDisplayGamut (UIDisplayGamut displayGamut);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UITraitCollection FromLayoutDirection (UITraitEnvironmentLayoutDirection layoutDirection);</span>
	<span class='added added-method ' data-is-non-breaking="">public UITraitCollection FromPreferredContentSizeCategory (UIContentSizeCategory category);</span>
</pre>
</div>

</div> <!-- end type UITraitCollection -->
<!-- start type UIView --> <div>
<h3>Type Changed: UIKit.UIView</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AssistiveTouchStatusDidChangeNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIFocusEnvironment[] PreferredFocusEnvironments { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static long TraitTabBar { get; }</span>
</pre>
</div>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public UIImage Capture (bool afterScreenUpdates);</span>
</pre>
</div>
<!-- start type UIView.Notifications --> <div>
<h3>Type Changed: UIKit.UIView.Notifications</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveAssistiveTouchStatusDidChange (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);</span>
</pre>
</div>

</div> <!-- end type UIView.Notifications -->

</div> <!-- end type UIView -->
<!-- start type UIViewController --> <div>
<h3>Type Changed: UIKit.UIViewController</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUIFocusEnvironment[] PreferredFocusEnvironments { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RestoresFocusAfterTransition { get; set; }</span>
</pre>
</div>

</div> <!-- end type UIViewController -->
<div> <!-- start type IUICollectionViewDataSourcePrefetching -->
<h3>New Type UIKit.IUICollectionViewDataSourcePrefetching</h3>
<pre class='added' data-is-non-breaking="">
public interface IUICollectionViewDataSourcePrefetching : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrefetchItems (UICollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type IUICollectionViewDataSourcePrefetching -->
<div> <!-- start type IUIContentSizeCategoryAdjusting -->
<h3>New Type UIKit.IUIContentSizeCategoryAdjusting</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIContentSizeCategoryAdjusting : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AdjustsFontForContentSizeCategory { get; set; }</span>
}
</pre>
</div> <!-- end type IUIContentSizeCategoryAdjusting -->
<div> <!-- start type IUIFocusItem -->
<h3>New Type UIKit.IUIFocusItem</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIFocusItem : ObjCRuntime.INativeObject, System.IDisposable, IUIFocusEnvironment {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanBecomeFocused { get; }</span>
}
</pre>
</div> <!-- end type IUIFocusItem -->
<div> <!-- start type IUITableViewDataSourcePrefetching -->
<h3>New Type UIKit.IUITableViewDataSourcePrefetching</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITableViewDataSourcePrefetching : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrefetchRows (UITableView tableView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type IUITableViewDataSourcePrefetching -->
<div> <!-- start type IUITimingCurveProvider -->
<h3>New Type UIKit.IUITimingCurveProvider</h3>
<pre class='added' data-is-non-breaking="">
public interface IUITimingCurveProvider : Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UICubicTimingParameters CubicTimingParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UISpringTimingParameters SpringTimingParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITimingCurveType TimingCurveType { get; }</span>
}
</pre>
</div> <!-- end type IUITimingCurveProvider -->
<div> <!-- start type IUIViewAnimating -->
<h3>New Type UIKit.IUIViewAnimating</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIViewAnimating : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FractionComplete { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Reversed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Running { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIViewAnimatingState State { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishAnimationAtPosition (UIViewAnimatingPosition finalPosition);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PauseAnimation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartAnimation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopAnimation (bool withoutFinishing);</span>
}
</pre>
</div> <!-- end type IUIViewAnimating -->
<div> <!-- start type IUIViewImplicitlyAnimating -->
<h3>New Type UIKit.IUIViewImplicitlyAnimating</h3>
<pre class='added' data-is-non-breaking="">
public interface IUIViewImplicitlyAnimating : ObjCRuntime.INativeObject, System.IDisposable, IUIViewAnimating {
}
</pre>
</div> <!-- end type IUIViewImplicitlyAnimating -->
<div> <!-- start type NSObject_UIAccessibilityCustomRotor -->
<h3>New Type UIKit.NSObject_UIAccessibilityCustomRotor</h3>
<pre class='added' data-is-non-breaking="">
public static class NSObject_UIAccessibilityCustomRotor {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UIAccessibilityCustomRotor[] GetAccessibilityCustomRotors (Foundation.NSObject This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetAccessibilityCustomRotors (Foundation.NSObject This, UIAccessibilityCustomRotor[] customRotors);</span>
}
</pre>
</div> <!-- end type NSObject_UIAccessibilityCustomRotor -->
<div> <!-- start type UIAccessibilityCustomRotor -->
<h3>New Type UIKit.UIAccessibilityCustomRotor</h3>
<pre class='added' data-is-non-breaking="">
public class UIAccessibilityCustomRotor : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotor ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityCustomRotor (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityCustomRotor (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotor (string name, UIAccessibilityCustomRotorSearch itemSearchHandler);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIAccessibilityCustomRotorSearch ItemSearchHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; set; }</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomRotor -->
<div> <!-- start type UIAccessibilityCustomRotorDirection -->
<h3>New Type UIKit.UIAccessibilityCustomRotorDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIAccessibilityCustomRotorDirection {
	<span class='added added-field ' data-is-non-breaking="">Next = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Previous = 0,</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomRotorDirection -->
<div> <!-- start type UIAccessibilityCustomRotorItemResult -->
<h3>New Type UIKit.UIAccessibilityCustomRotorItemResult</h3>
<pre class='added' data-is-non-breaking="">
public class UIAccessibilityCustomRotorItemResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotorItemResult ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityCustomRotorItemResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityCustomRotorItemResult (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotorItemResult (Foundation.NSObject targetElement, UITextRange targetRange);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject TargetElement { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITextRange TargetRange { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomRotorItemResult -->
<div> <!-- start type UIAccessibilityCustomRotorSearch -->
<h3>New Type UIKit.UIAccessibilityCustomRotorSearch</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate UIAccessibilityCustomRotorSearch : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotorSearch (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UIAccessibilityCustomRotorSearchPredicate predicate, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIAccessibilityCustomRotorItemResult EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual UIAccessibilityCustomRotorItemResult Invoke (UIAccessibilityCustomRotorSearchPredicate predicate);</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomRotorSearch -->
<div> <!-- start type UIAccessibilityCustomRotorSearchPredicate -->
<h3>New Type UIKit.UIAccessibilityCustomRotorSearchPredicate</h3>
<pre class='added' data-is-non-breaking="">
public class UIAccessibilityCustomRotorSearchPredicate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIAccessibilityCustomRotorSearchPredicate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityCustomRotorSearchPredicate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIAccessibilityCustomRotorSearchPredicate (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIAccessibilityCustomRotorItemResult CurrentItem { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIAccessibilityCustomRotorDirection SearchDirection { get; set; }</span>
}
</pre>
</div> <!-- end type UIAccessibilityCustomRotorSearchPredicate -->
<div> <!-- start type UICollectionViewDataSourcePrefetching_Extensions -->
<h3>New Type UIKit.UICollectionViewDataSourcePrefetching_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UICollectionViewDataSourcePrefetching_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelPrefetching (IUICollectionViewDataSourcePrefetching This, UICollectionView collectionView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type UICollectionViewDataSourcePrefetching_Extensions -->
<div> <!-- start type UIContentSizeCategoryExtensions -->
<h3>New Type UIKit.UIContentSizeCategoryExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIContentSizeCategoryExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetConstant (UIContentSizeCategory self);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIContentSizeCategory GetValue (Foundation.NSString constant);</span>
}
</pre>
</div> <!-- end type UIContentSizeCategoryExtensions -->
<div> <!-- start type UICubicTimingParameters -->
<h3>New Type UIKit.UICubicTimingParameters</h3>
<pre class='added' data-is-non-breaking="">
public class UICubicTimingParameters : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUITimingCurveProvider {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UICubicTimingParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UICubicTimingParameters (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICubicTimingParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UICubicTimingParameters (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UICubicTimingParameters (UIViewAnimationCurve curve);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UICubicTimingParameters (CoreGraphics.CGPoint point1, CoreGraphics.CGPoint point2);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UIViewAnimationCurve AnimationCurve { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint ControlPoint1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGPoint ControlPoint2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UICubicTimingParameters CubicTimingParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UISpringTimingParameters SpringTimingParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITimingCurveType TimingCurveType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type UICubicTimingParameters -->
<div> <!-- start type UIDisplayGamut -->
<h3>New Type UIKit.UIDisplayGamut</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIDisplayGamut {
	<span class='added added-field ' data-is-non-breaking="">P3 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Srgb = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = -1,</span>
}
</pre>
</div> <!-- end type UIDisplayGamut -->
<div> <!-- start type UIFocusEnvironment_Extensions -->
<h3>New Type UIKit.UIFocusEnvironment_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIFocusEnvironment_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static IUIFocusEnvironment[] GetPreferredFocusEnvironments (IUIFocusEnvironment This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetPreferredFocusEnvironments (IUIFocusEnvironment This, IUIFocusEnvironment[] value);</span>
}
</pre>
</div> <!-- end type UIFocusEnvironment_Extensions -->
<div> <!-- start type UIGraphicsImageRenderer -->
<h3>New Type UIKit.UIGraphicsImageRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsImageRenderer : UIKit.UIGraphicsRenderer, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsImageRenderer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsImageRenderer (CoreGraphics.CGSize size);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsImageRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsImageRenderer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsImageRenderer (CoreGraphics.CGRect bounds, UIGraphicsImageRendererFormat format);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsImageRenderer (CoreGraphics.CGSize size, UIGraphicsImageRendererFormat format);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual UIImage CreateImage (System.Action&lt;UIGraphicsImageRendererContext&gt; actions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData CreateJpeg (nfloat compressionQuality, System.Action&lt;UIGraphicsImageRendererContext&gt; actions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData CreatePng (System.Action&lt;UIGraphicsImageRendererContext&gt; actions);</span>
}
</pre>
</div> <!-- end type UIGraphicsImageRenderer -->
<div> <!-- start type UIGraphicsImageRendererContext -->
<h3>New Type UIKit.UIGraphicsImageRendererContext</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsImageRendererContext : UIKit.UIGraphicsRendererContext, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsImageRendererContext ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsImageRendererContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsImageRendererContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIImage CurrentImage { get; }</span>
}
</pre>
</div> <!-- end type UIGraphicsImageRendererContext -->
<div> <!-- start type UIGraphicsImageRendererFormat -->
<h3>New Type UIKit.UIGraphicsImageRendererFormat</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsImageRendererFormat : UIKit.UIGraphicsRendererFormat, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsImageRendererFormat ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsImageRendererFormat (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsImageRendererFormat (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Opaque { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrefersExtendedRange { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat Scale { get; set; }</span>
}
</pre>
</div> <!-- end type UIGraphicsImageRendererFormat -->
<div> <!-- start type UIGraphicsPdfRenderer -->
<h3>New Type UIKit.UIGraphicsPdfRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsPdfRenderer : UIKit.UIGraphicsRenderer, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsPdfRenderer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsPdfRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsPdfRenderer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsPdfRenderer (CoreGraphics.CGRect bounds, UIGraphicsPdfRendererFormat format);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSData CreatePdf (System.Action&lt;UIGraphicsPdfRendererContext&gt; actions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool WritePdf (Foundation.NSUrl url, System.Action&lt;UIGraphicsPdfRendererContext&gt; actions, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type UIGraphicsPdfRenderer -->
<div> <!-- start type UIGraphicsPdfRendererContext -->
<h3>New Type UIKit.UIGraphicsPdfRendererContext</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsPdfRendererContext : UIKit.UIGraphicsRendererContext, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsPdfRendererContext ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsPdfRendererContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsPdfRendererContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect PdfContextBounds { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddDestination (string name, CoreGraphics.CGPoint point);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginPage ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginPage (CoreGraphics.CGRect bounds, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; pageInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetDestination (string name, CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SetUrl (Foundation.NSUrl url, CoreGraphics.CGRect rect);</span>
}
</pre>
</div> <!-- end type UIGraphicsPdfRendererContext -->
<div> <!-- start type UIGraphicsPdfRendererFormat -->
<h3>New Type UIKit.UIGraphicsPdfRendererFormat</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsPdfRendererFormat : UIKit.UIGraphicsRendererFormat, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsPdfRendererFormat ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsPdfRendererFormat (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsPdfRendererFormat (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; DocumentInfo { get; set; }</span>
}
</pre>
</div> <!-- end type UIGraphicsPdfRendererFormat -->
<div> <!-- start type UIGraphicsRenderer -->
<h3>New Type UIKit.UIGraphicsRenderer</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsRenderer : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsRenderer ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsRenderer (CoreGraphics.CGRect bounds);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsRenderer (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsRenderer (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsRenderer (CoreGraphics.CGRect bounds, UIGraphicsRendererFormat format);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsImageOutput { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIGraphicsRendererFormat Format { get; }</span>
}
</pre>
</div> <!-- end type UIGraphicsRenderer -->
<div> <!-- start type UIGraphicsRendererContext -->
<h3>New Type UIKit.UIGraphicsRendererContext</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsRendererContext : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsRendererContext ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsRendererContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsRendererContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGContext CGContext { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIGraphicsRendererFormat Format { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void ClipToRect (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FillRect (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FillRect (CoreGraphics.CGRect rect, CoreGraphics.CGBlendMode blendMode);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StrokeRect (CoreGraphics.CGRect rect);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StrokeRect (CoreGraphics.CGRect rect, CoreGraphics.CGBlendMode blendMode);</span>
}
</pre>
</div> <!-- end type UIGraphicsRendererContext -->
<div> <!-- start type UIGraphicsRendererFormat -->
<h3>New Type UIKit.UIGraphicsRendererFormat</h3>
<pre class='added' data-is-non-breaking="">
public class UIGraphicsRendererFormat : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIGraphicsRendererFormat ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsRendererFormat (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIGraphicsRendererFormat (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect Bounds { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static UIGraphicsRendererFormat DefaultFormat { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type UIGraphicsRendererFormat -->
<div> <!-- start type UISpringTimingParameters -->
<h3>New Type UIKit.UISpringTimingParameters</h3>
<pre class='added' data-is-non-breaking="">
public class UISpringTimingParameters : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUITimingCurveProvider {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UISpringTimingParameters ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISpringTimingParameters (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UISpringTimingParameters (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UISpringTimingParameters (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISpringTimingParameters (nfloat ratio);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISpringTimingParameters (nfloat ratio, CoreGraphics.CGVector velocity);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UISpringTimingParameters (nfloat mass, nfloat stiffness, nfloat damping, CoreGraphics.CGVector velocity);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UICubicTimingParameters CubicTimingParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGVector InitialVelocity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UISpringTimingParameters SpringTimingParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UITimingCurveType TimingCurveType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type UISpringTimingParameters -->
<div> <!-- start type UITableViewDataSourcePrefetching_Extensions -->
<h3>New Type UIKit.UITableViewDataSourcePrefetching_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITableViewDataSourcePrefetching_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelPrefetching (IUITableViewDataSourcePrefetching This, UITableView tableView, Foundation.NSIndexPath[] indexPaths);</span>
}
</pre>
</div> <!-- end type UITableViewDataSourcePrefetching_Extensions -->
<div> <!-- start type UITextContentType -->
<h3>New Type UIKit.UITextContentType</h3>
<pre class='added' data-is-non-breaking="">
public static class UITextContentType {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AddressCity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AddressCityAndState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString AddressState { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CountryName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CreditCardNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString EmailAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FamilyName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString FullStreetAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString GivenName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString JobTitle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString MiddleName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NamePrefix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString NameSuffix { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Nickname { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString OrganizationName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString PostalCode { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StreetAddressLine1 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString StreetAddressLine2 { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Sublocality { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString TelephoneNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Url { get; }</span>
}
</pre>
</div> <!-- end type UITextContentType -->
<div> <!-- start type UITextDocumentProxy_Extensions -->
<h3>New Type UIKit.UITextDocumentProxy_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITextDocumentProxy_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UITextInputMode GetDocumentInputMode (IUITextDocumentProxy This);</span>
}
</pre>
</div> <!-- end type UITextDocumentProxy_Extensions -->
<div> <!-- start type UITextInputTraits_Extensions -->
<h3>New Type UIKit.UITextInputTraits_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UITextInputTraits_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetTextContentType (IUITextInputTraits This);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void SetTextContentType (IUITextInputTraits This, Foundation.NSString value);</span>
}
</pre>
</div> <!-- end type UITextInputTraits_Extensions -->
<div> <!-- start type UITextItemInteraction -->
<h3>New Type UIKit.UITextItemInteraction</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITextItemInteraction {
	<span class='added added-field ' data-is-non-breaking="">InvokeDefaultAction = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PresentActions = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Preview = 2,</span>
}
</pre>
</div> <!-- end type UITextItemInteraction -->
<div> <!-- start type UITimingCurveType -->
<h3>New Type UIKit.UITimingCurveType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITimingCurveType {
	<span class='added added-field ' data-is-non-breaking="">Builtin = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Composed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Cubic = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Spring = 2,</span>
}
</pre>
</div> <!-- end type UITimingCurveType -->
<div> <!-- start type UITraitEnvironmentLayoutDirection -->
<h3>New Type UIKit.UITraitEnvironmentLayoutDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UITraitEnvironmentLayoutDirection {
	<span class='added added-field ' data-is-non-breaking="">LeftToRight = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RightToLeft = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = -1,</span>
}
</pre>
</div> <!-- end type UITraitEnvironmentLayoutDirection -->
<div> <!-- start type UIUserInterfaceStyle -->
<h3>New Type UIKit.UIUserInterfaceStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIUserInterfaceStyle {
	<span class='added added-field ' data-is-non-breaking="">Dark = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Light = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unspecified = 0,</span>
}
</pre>
</div> <!-- end type UIUserInterfaceStyle -->
<div> <!-- start type UIViewAnimatingPosition -->
<h3>New Type UIKit.UIViewAnimatingPosition</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIViewAnimatingPosition {
	<span class='added added-field ' data-is-non-breaking="">Current = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">End = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Start = 1,</span>
}
</pre>
</div> <!-- end type UIViewAnimatingPosition -->
<div> <!-- start type UIViewAnimatingState -->
<h3>New Type UIKit.UIViewAnimatingState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UIViewAnimatingState {
	<span class='added added-field ' data-is-non-breaking="">Active = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Inactive = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Stopped = 2,</span>
}
</pre>
</div> <!-- end type UIViewAnimatingState -->
<div> <!-- start type UIViewImplicitlyAnimating_Extensions -->
<h3>New Type UIKit.UIViewImplicitlyAnimating_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UIViewImplicitlyAnimating_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void AddAnimations (IUIViewImplicitlyAnimating This, System.Action animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void AddAnimations (IUIViewImplicitlyAnimating This, System.Action animation, nfloat delayFactor);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void AddCompletion (IUIViewImplicitlyAnimating This, System.Action&lt;UIViewAnimatingPosition&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void ContinueAnimation (IUIViewImplicitlyAnimating This, IUITimingCurveProvider parameters, nfloat durationFactor);</span>
}
</pre>
</div> <!-- end type UIViewImplicitlyAnimating_Extensions -->
<div> <!-- start type UIViewPropertyAnimator -->
<h3>New Type UIKit.UIViewPropertyAnimator</h3>
<pre class='added' data-is-non-breaking="">
public class UIViewPropertyAnimator : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUIViewAnimating, IUIViewImplicitlyAnimating {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UIViewPropertyAnimator ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIViewPropertyAnimator (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UIViewPropertyAnimator (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIViewPropertyAnimator (double duration, IUITimingCurveProvider parameters);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIViewPropertyAnimator (double duration, nfloat ratio, System.Action animations);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIViewPropertyAnimator (double duration, UIViewAnimationCurve curve, System.Action animations);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UIViewPropertyAnimator (double duration, CoreGraphics.CGPoint point1, CoreGraphics.CGPoint point2, System.Action animations);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat FractionComplete { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Interruptible { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Reversed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Running { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIViewAnimatingState State { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUITimingCurveProvider TimingParameters { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UserInteractionEnabled { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimations (System.Action animation);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAnimations (System.Action animation, nfloat delayFactor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddCompletion (System.Action&lt;UIViewAnimatingPosition&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ContinueAnimation (IUITimingCurveProvider timingParameters, nfloat durationFactor);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIViewPropertyAnimator CreateRunningProperty (double duration, double delay, UIViewAnimationOptions options, System.Action animations, System.Action&lt;UIViewAnimatingPosition&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishAnimationAtPosition (UIViewAnimatingPosition finalPosition);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PauseAnimation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartAnimation ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopAnimation (bool withoutFinishing);</span>
}
</pre>
</div> <!-- end type UIViewPropertyAnimator -->

</div> <!-- end namespace UIKit -->
<!-- start namespace ExternalAccessory --> <div> 
<h2>New Namespace ExternalAccessory</h2>

<div> <!-- start type EAAccessory -->
<h3>New Type ExternalAccessory.EAAccessory</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Connected { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint ConnectionID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IEAAccessoryDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DockType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FirmwareRevision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string HardwareRevision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ModelNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] ProtocolStrings { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SerialNumber { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler Disconnected;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type EAAccessory -->
<div> <!-- start type EAAccessoryDelegate -->
<h3>New Type ExternalAccessory.EAAccessoryDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessoryDelegate : Foundation.NSObject, IEAAccessoryDelegate, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EAAccessoryDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Disconnected (EAAccessory accessory);</span>
}
</pre>
</div> <!-- end type EAAccessoryDelegate -->
<div> <!-- start type EAAccessoryDelegate_Extensions -->
<h3>New Type ExternalAccessory.EAAccessoryDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class EAAccessoryDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void Disconnected (IEAAccessoryDelegate This, EAAccessory accessory);</span>
}
</pre>
</div> <!-- end type EAAccessoryDelegate_Extensions -->
<div> <!-- start type EAAccessoryEventArgs -->
<h3>New Type ExternalAccessory.EAAccessoryEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessoryEventArgs : Foundation.NSNotificationEventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EAAccessoryEventArgs (Foundation.NSNotification notification);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public EAAccessory Accessory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public EAAccessory Selected { get; }</span>
}
</pre>
</div> <!-- end type EAAccessoryEventArgs -->
<div> <!-- start type EAAccessoryManager -->
<h3>New Type ExternalAccessory.EAAccessoryManager</h3>
<pre class='added' data-is-non-breaking="">
public class EAAccessoryManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAAccessoryManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual EAAccessory[] ConnectedAccessories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidConnectNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString DidDisconnectNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static EAAccessoryManager SharedAccessoryManager { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterForLocalNotifications ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ShowBluetoothAccessoryPicker (Foundation.NSPredicate predicate, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ShowBluetoothAccessoryPickerAsync (Foundation.NSPredicate predicate);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnregisterForLocalNotifications ();</span>

	// inner types
	public static class Notifications {
		// methods
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidConnect (System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
		<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSObject ObserveDidDisconnect (System.EventHandler&lt;EAAccessoryEventArgs&gt; handler);</span>
	}
}
</pre>
</div> <!-- end type EAAccessoryManager -->
<div> <!-- start type EABluetoothAccessoryPickerError -->
<h3>New Type ExternalAccessory.EABluetoothAccessoryPickerError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum EABluetoothAccessoryPickerError {
	<span class='added added-field ' data-is-non-breaking="">AlreadyConnected = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Failed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NotFound = 1,</span>
}
</pre>
</div> <!-- end type EABluetoothAccessoryPickerError -->
<div> <!-- start type EABluetoothAccessoryPickerErrorExtensions -->
<h3>New Type ExternalAccessory.EABluetoothAccessoryPickerErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class EABluetoothAccessoryPickerErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (EABluetoothAccessoryPickerError self);</span>
}
</pre>
</div> <!-- end type EABluetoothAccessoryPickerErrorExtensions -->
<div> <!-- start type EASession -->
<h3>New Type ExternalAccessory.EASession</h3>
<pre class='added' data-is-non-breaking="">
public class EASession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected EASession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EASession (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public EASession (EAAccessory accessory, string protocol);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual EAAccessory Accessory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSInputStream InputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSOutputStream OutputStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ProtocolString { get; }</span>
}
</pre>
</div> <!-- end type EASession -->
<div> <!-- start type EAWiFiUnconfiguredAccessory -->
<h3>New Type ExternalAccessory.EAWiFiUnconfiguredAccessory</h3>
<pre class='added' data-is-non-breaking="">
public class EAWiFiUnconfiguredAccessory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EAWiFiUnconfiguredAccessory ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAWiFiUnconfiguredAccessory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAWiFiUnconfiguredAccessory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string MacAddress { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Manufacturer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Model { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual EAWiFiUnconfiguredAccessoryProperties Properties { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Ssid { get; }</span>
}
</pre>
</div> <!-- end type EAWiFiUnconfiguredAccessory -->
<div> <!-- start type EAWiFiUnconfiguredAccessoryBrowser -->
<h3>New Type ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowser</h3>
<pre class='added' data-is-non-breaking="">
public class EAWiFiUnconfiguredAccessoryBrowser : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public EAWiFiUnconfiguredAccessoryBrowser ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAWiFiUnconfiguredAccessoryBrowser (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected EAWiFiUnconfiguredAccessoryBrowser (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet UnconfiguredAccessories { get; }</span>
}
</pre>
</div> <!-- end type EAWiFiUnconfiguredAccessoryBrowser -->
<div> <!-- start type EAWiFiUnconfiguredAccessoryBrowserState -->
<h3>New Type ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum EAWiFiUnconfiguredAccessoryBrowserState {
	<span class='added added-field ' data-is-non-breaking="">Configuring = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Searching = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Stopped = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">WiFiUnavailable = 0,</span>
}
</pre>
</div> <!-- end type EAWiFiUnconfiguredAccessoryBrowserState -->
<div> <!-- start type EAWiFiUnconfiguredAccessoryConfigurationStatus -->
<h3>New Type ExternalAccessory.EAWiFiUnconfiguredAccessoryConfigurationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum EAWiFiUnconfiguredAccessoryConfigurationStatus {
	<span class='added added-field ' data-is-non-breaking="">Failed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Success = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserCancelledConfiguration = 1,</span>
}
</pre>
</div> <!-- end type EAWiFiUnconfiguredAccessoryConfigurationStatus -->
<div> <!-- start type EAWiFiUnconfiguredAccessoryProperties -->
<h3>New Type ExternalAccessory.EAWiFiUnconfiguredAccessoryProperties</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum EAWiFiUnconfiguredAccessoryProperties {
	<span class='added added-field ' data-is-non-breaking="">SupportsAirPlay = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">SupportsAirPrint = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">SupportsHomeKit = 4,</span>
}
</pre>
</div> <!-- end type EAWiFiUnconfiguredAccessoryProperties -->
<div> <!-- start type IEAAccessoryDelegate -->
<h3>New Type ExternalAccessory.IEAAccessoryDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IEAAccessoryDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IEAAccessoryDelegate -->
</div> <!-- end namespace ExternalAccessory -->

<!-- start namespace HomeKit --> <div> 
<h2>New Namespace HomeKit</h2>

<div> <!-- start type HMAccessory -->
<h3>New Type HomeKit.HMAccessory</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessory ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Blocked { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Bridged { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraProfile[] CameraProfiles { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessoryCategory Category { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IHMAccessoryDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Reachable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMRoom Room { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMService[] Services { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid[] UniqueIdentifiersForBridgedAccessories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryUpdateEventArgs&gt; DidUpdateAssociatedServiceType;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateName;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryUpdateEventArgs&gt; DidUpdateNameForService;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateReachability;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateServices;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMAccessoryServiceUpdateCharacteristicEventArgs&gt; DidUpdateValueForCharacteristic;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Identify (System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task IdentifyAsync ();</span>
}
</pre>
</div> <!-- end type HMAccessory -->
<div> <!-- start type HMAccessoryCategory -->
<h3>New Type HomeKit.HMAccessoryCategory</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryCategory : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessoryCategory (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessoryCategory (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMAccessoryCategoryType CategoryType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedDescription { get; }</span>
}
</pre>
</div> <!-- end type HMAccessoryCategory -->
<div> <!-- start type HMAccessoryCategoryType -->
<h3>New Type HomeKit.HMAccessoryCategoryType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMAccessoryCategoryType {
	<span class='added added-field ' data-is-non-breaking="">Bridge = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Door = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">DoorLock = 4,</span>

	<span class='added added-field ' data-is-non-breaking="">[Obsolete ("Use GarageDoorOpener instead")]
	DoorOpener = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Fan = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">GarageDoorOpener = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">IPCamera = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Lightbulb = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Other = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Outlet = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ProgrammableSwitch = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">RangeExtender = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SecuritySystem = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Sensor = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Switch = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Thermostat = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoDoorbell = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Window = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">WindowCovering = 14,</span>
}
</pre>
</div> <!-- end type HMAccessoryCategoryType -->
<div> <!-- start type HMAccessoryDelegate -->
<h3>New Type HomeKit.HMAccessoryDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IHMAccessoryDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessoryDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessoryDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateAssociatedServiceType (HMAccessory accessory, HMService service);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateName (HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNameForService (HMAccessory accessory, HMService service);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateReachability (HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateServices (HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateValueForCharacteristic (HMAccessory accessory, HMService service, HMCharacteristic characteristic);</span>
}
</pre>
</div> <!-- end type HMAccessoryDelegate -->
<div> <!-- start type HMAccessoryDelegate_Extensions -->
<h3>New Type HomeKit.HMAccessoryDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMAccessoryDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateAssociatedServiceType (IHMAccessoryDelegate This, HMAccessory accessory, HMService service);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateName (IHMAccessoryDelegate This, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNameForService (IHMAccessoryDelegate This, HMAccessory accessory, HMService service);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateReachability (IHMAccessoryDelegate This, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateServices (IHMAccessoryDelegate This, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateValueForCharacteristic (IHMAccessoryDelegate This, HMAccessory accessory, HMService service, HMCharacteristic characteristic);</span>
}
</pre>
</div> <!-- end type HMAccessoryDelegate_Extensions -->
<div> <!-- start type HMAccessoryProfile -->
<h3>New Type HomeKit.HMAccessoryProfile</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryProfile : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessoryProfile (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAccessoryProfile (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessory Accessory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMService[] Services { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type HMAccessoryProfile -->
<div> <!-- start type HMAccessoryServiceUpdateCharacteristicEventArgs -->
<h3>New Type HomeKit.HMAccessoryServiceUpdateCharacteristicEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryServiceUpdateCharacteristicEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryServiceUpdateCharacteristicEventArgs (HMService service, HMCharacteristic characteristic);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMCharacteristic Characteristic { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HMService Service { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryServiceUpdateCharacteristicEventArgs -->
<div> <!-- start type HMAccessoryUpdateEventArgs -->
<h3>New Type HomeKit.HMAccessoryUpdateEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMAccessoryUpdateEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAccessoryUpdateEventArgs (HMService service);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMService Service { get; set; }</span>
}
</pre>
</div> <!-- end type HMAccessoryUpdateEventArgs -->
<div> <!-- start type HMAction -->
<h3>New Type HomeKit.HMAction</h3>
<pre class='added' data-is-non-breaking="">
public class HMAction : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMAction ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMAction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMAction -->
<div> <!-- start type HMActionSet -->
<h3>New Type HomeKit.HMActionSet</h3>
<pre class='added' data-is-non-breaking="">
public class HMActionSet : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMActionSet (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMActionSet (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMActionSetType ActionSetType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSet Actions { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Executing { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate LastExecutionDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMActionSet -->
<div> <!-- start type HMActionSetType -->
<h3>New Type HomeKit.HMActionSetType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMActionSetType {
	<span class='added added-field ' data-is-non-breaking="">HomeArrival = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeDeparture = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Sleep = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TriggerOwned = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = -1,</span>
	<span class='added added-field ' data-is-non-breaking="">UserDefined = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">WakeUp = 0,</span>
}
</pre>
</div> <!-- end type HMActionSetType -->
<div> <!-- start type HMCameraAudioControl -->
<h3>New Type HomeKit.HMCameraAudioControl</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraAudioControl : HomeKit.HMCameraControl, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraAudioControl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraAudioControl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic Mute { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic Volume { get; }</span>
}
</pre>
</div> <!-- end type HMCameraAudioControl -->
<div> <!-- start type HMCameraAudioStreamSetting -->
<h3>New Type HomeKit.HMCameraAudioStreamSetting</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCameraAudioStreamSetting {
	<span class='added added-field ' data-is-non-breaking="">BidirectionalAudioAllowed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">IncomingAudioAllowed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Muted = 1,</span>
}
</pre>
</div> <!-- end type HMCameraAudioStreamSetting -->
<div> <!-- start type HMCameraControl -->
<h3>New Type HomeKit.HMCameraControl</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraControl : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraControl ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraControl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraControl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMCameraControl -->
<div> <!-- start type HMCameraProfile -->
<h3>New Type HomeKit.HMCameraProfile</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraProfile : HomeKit.HMAccessoryProfile, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraProfile (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraProfile (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraAudioControl MicrophoneControl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraSettingsControl SettingsControl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraSnapshotControl SnapshotControl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraAudioControl SpeakerControl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraStreamControl StreamControl { get; }</span>
}
</pre>
</div> <!-- end type HMCameraProfile -->
<div> <!-- start type HMCameraSettingsControl -->
<h3>New Type HomeKit.HMCameraSettingsControl</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraSettingsControl : HomeKit.HMCameraControl, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSettingsControl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSettingsControl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic CurrentHorizontalTilt { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic CurrentVerticalTilt { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic DigitalZoom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic ImageMirroring { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic ImageRotation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic NightVision { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic OpticalZoom { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic TargetHorizontalTilt { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic TargetVerticalTilt { get; }</span>
}
</pre>
</div> <!-- end type HMCameraSettingsControl -->
<div> <!-- start type HMCameraSnapshot -->
<h3>New Type HomeKit.HMCameraSnapshot</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraSnapshot : HomeKit.HMCameraSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraSnapshot ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSnapshot (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSnapshot (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CaptureDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMCameraSnapshot -->
<div> <!-- start type HMCameraSnapshotControl -->
<h3>New Type HomeKit.HMCameraSnapshotControl</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraSnapshotControl : HomeKit.HMCameraControl, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraSnapshotControl ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSnapshotControl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSnapshotControl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IHMCameraSnapshotControlDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraSnapshot MostRecentSnapshot { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void TakeSnapshot ();</span>
}
</pre>
</div> <!-- end type HMCameraSnapshotControl -->
<div> <!-- start type HMCameraSnapshotControlDelegate -->
<h3>New Type HomeKit.HMCameraSnapshotControlDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraSnapshotControlDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IHMCameraSnapshotControlDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraSnapshotControlDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSnapshotControlDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSnapshotControlDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidTakeSnapshot (HMCameraSnapshotControl cameraSnapshotControl, HMCameraSnapshot snapshot, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type HMCameraSnapshotControlDelegate -->
<div> <!-- start type HMCameraSnapshotControlDelegate_Extensions -->
<h3>New Type HomeKit.HMCameraSnapshotControlDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMCameraSnapshotControlDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidTakeSnapshot (IHMCameraSnapshotControlDelegate This, HMCameraSnapshotControl cameraSnapshotControl, HMCameraSnapshot snapshot, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type HMCameraSnapshotControlDelegate_Extensions -->
<div> <!-- start type HMCameraSource -->
<h3>New Type HomeKit.HMCameraSource</h3>
<pre class='added' data-is-non-breaking="">
public abstract class HMCameraSource : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSource ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraSource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMCameraSource -->
<div> <!-- start type HMCameraStream -->
<h3>New Type HomeKit.HMCameraStream</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraStream : HomeKit.HMCameraSource, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraStream ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraStream (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraStream (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMCameraStream -->
<div> <!-- start type HMCameraStreamControl -->
<h3>New Type HomeKit.HMCameraStreamControl</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraStreamControl : HomeKit.HMCameraControl, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraStreamControl ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraStreamControl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraStreamControl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraStream CameraStream { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IHMCameraStreamControlDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraStreamState StreamState { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartStream ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopStream ();</span>
}
</pre>
</div> <!-- end type HMCameraStreamControl -->
<div> <!-- start type HMCameraStreamControlDelegate -->
<h3>New Type HomeKit.HMCameraStreamControlDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraStreamControlDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IHMCameraStreamControlDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraStreamControlDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraStreamControlDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraStreamControlDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStartStream (HMCameraStreamControl cameraStreamControl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStopStream (HMCameraStreamControl cameraStreamControl, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type HMCameraStreamControlDelegate -->
<div> <!-- start type HMCameraStreamControlDelegate_Extensions -->
<h3>New Type HomeKit.HMCameraStreamControlDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMCameraStreamControlDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidStartStream (IHMCameraStreamControlDelegate This, HMCameraStreamControl cameraStreamControl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidStopStream (IHMCameraStreamControlDelegate This, HMCameraStreamControl cameraStreamControl, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type HMCameraStreamControlDelegate_Extensions -->
<div> <!-- start type HMCameraStreamState -->
<h3>New Type HomeKit.HMCameraStreamState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCameraStreamState {
	<span class='added added-field ' data-is-non-breaking="">NotStreaming = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Starting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Stopping = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Streaming = 2,</span>
}
</pre>
</div> <!-- end type HMCameraStreamState -->
<div> <!-- start type HMCameraView -->
<h3>New Type HomeKit.HMCameraView</h3>
<pre class='added' data-is-non-breaking="">
public class HMCameraView : UIKit.UIView, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public HMCameraView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static HMCameraView.HMCameraViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCameraSource CameraSource { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static HMCameraView.HMCameraViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMCameraView.HMCameraViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMCameraView.HMCameraViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMCameraView.HMCameraViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMCameraView.HMCameraViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static HMCameraView.HMCameraViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>

	// inner types
	public class HMCameraViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected HMCameraView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type HMCameraView -->
<div> <!-- start type HMCharacteristic -->
<h3>New Type HomeKit.HMCharacteristic</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristic : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCharacteristic ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristic (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristic (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMCharacteristicType CharacteristicType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Hidden { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString KeyPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristicMetadata Metadata { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NotificationEnabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSString[] Properties { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Readable { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMService Service { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool SupportsEventNotification { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject Value { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ValueKeyPath { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Writable { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnableNotification (bool enable, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task EnableNotificationAsync (bool enable);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReadValue (System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ReadValueAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteValue (Foundation.NSObject value, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task WriteValueAsync (Foundation.NSObject value);</span>
}
</pre>
</div> <!-- end type HMCharacteristic -->
<div> <!-- start type HMCharacteristicEvent -->
<h3>New Type HomeKit.HMCharacteristicEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristicEvent : HomeKit.HMEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic Characteristic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.INSCopying TriggerValue { get; }</span>
}
</pre>
</div> <!-- end type HMCharacteristicEvent -->
<div> <!-- start type HMCharacteristicMetadata -->
<h3>New Type HomeKit.HMCharacteristicMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristicMetadata : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCharacteristicMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicMetadata (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicMetadata (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HMCharacteristicMetadataFormat Format { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ManufacturerDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber MaxLength { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber MaximumValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber MinimumValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber StepValue { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HMCharacteristicMetadataUnits Units { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber[] ValidValues { get; }</span>
}
</pre>
</div> <!-- end type HMCharacteristicMetadata -->
<div> <!-- start type HMCharacteristicMetadataFormat -->
<h3>New Type HomeKit.HMCharacteristicMetadataFormat</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicMetadataFormat {
	<span class='added added-field ' data-is-non-breaking="">Array = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Bool = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Data = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">Dictionary = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Float = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Int = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">String = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Tlv8 = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt16 = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt32 = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt64 = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">UInt8 = 7,</span>
}
</pre>
</div> <!-- end type HMCharacteristicMetadataFormat -->
<div> <!-- start type HMCharacteristicMetadataUnits -->
<h3>New Type HomeKit.HMCharacteristicMetadataUnits</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicMetadataUnits {
	<span class='added added-field ' data-is-non-breaking="">ArcDegree = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Celsius = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Fahrenheit = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Lux = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">MicrogramsPerCubicMeter = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PartsPerMillion = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">Percentage = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Seconds = 5,</span>
}
</pre>
</div> <!-- end type HMCharacteristicMetadataUnits -->
<div> <!-- start type HMCharacteristicProperties -->
<h3>New Type HomeKit.HMCharacteristicProperties</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristicProperties {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMCharacteristicProperties ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool Readable { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool SupportsBonjourNotification { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool SupportsChangeNumber { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool SupportsEventNotification { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Writable { get; set; }</span>
}
</pre>
</div> <!-- end type HMCharacteristicProperties -->
<div> <!-- start type HMCharacteristicType -->
<h3>New Type HomeKit.HMCharacteristicType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicType {
	<span class='added added-field ' data-is-non-breaking="">AdminOnlyAccess = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">AirParticulateDensity = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">AirParticulateSize = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">AirQuality = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">AudioFeedback = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">BatteryLevel = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">Brightness = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonDioxideDetected = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonDioxideLevel = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonDioxidePeakLevel = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonMonoxideDetected = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonMonoxideLevel = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonMonoxidePeakLevel = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">ChargingState = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">ContactState = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">CoolingThreshold = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentDoorState = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentHeatingCooling = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentHorizontalTilt = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentLightLevel = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentLockMechanismState = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentPosition = 51,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentRelativeHumidity = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentSecuritySystemState = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentTemperature = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">CurrentVerticalTilt = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">DigitalZoom = 82,</span>
	<span class='added added-field ' data-is-non-breaking="">FirmwareVersion = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">HardwareVersion = 54,</span>
	<span class='added added-field ' data-is-non-breaking="">HeatingCoolingStatus = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">HeatingThreshold = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">HoldPosition = 55,</span>
	<span class='added added-field ' data-is-non-breaking="">Hue = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Identify = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageMirroring = 84,</span>
	<span class='added added-field ' data-is-non-breaking="">ImageRotation = 83,</span>
	<span class='added added-field ' data-is-non-breaking="">InputEvent = 56,</span>
	<span class='added added-field ' data-is-non-breaking="">LeakDetected = 57,</span>
	<span class='added added-field ' data-is-non-breaking="">LockManagementAutoSecureTimeout = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">LockManagementControlPoint = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">LockMechanismLastKnownAction = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">Logs = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">Manufacturer = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">Model = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">MotionDetected = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">Mute = 79,</span>
	<span class='added added-field ' data-is-non-breaking="">Name = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">NightVision = 80,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">ObstructionDetected = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">OccupancyDetected = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">OpticalZoom = 81,</span>
	<span class='added added-field ' data-is-non-breaking="">OutletInUse = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">OutputState = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">PositionState = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">PowerState = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">RotationDirection = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">RotationSpeed = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">Saturation = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SelectedStreamConfiguration = 77,</span>
	<span class='added added-field ' data-is-non-breaking="">SerialNumber = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">SetupStreamEndpoint = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">SmokeDetected = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">SoftwareVersion = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusActive = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusFault = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusJammed = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusLowBattery = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">StatusTampered = 67,</span>
	<span class='added added-field ' data-is-non-breaking="">StreamingStatus = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">SupportedAudioStreamConfiguration = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">SupportedRtpConfiguration = 76,</span>
	<span class='added added-field ' data-is-non-breaking="">SupportedVideoStreamConfiguration = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetDoorState = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetHeatingCooling = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetHorizontalTilt = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetLockMechanismState = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetPosition = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetRelativeHumidity = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetSecuritySystemState = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetTemperature = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">TargetVerticalTilt = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">TemperatureUnits = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Version = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">Volume = 78,</span>
}
</pre>
</div> <!-- end type HMCharacteristicType -->
<div> <!-- start type HMCharacteristicValueAirParticulate -->
<h3>New Type HomeKit.HMCharacteristicValueAirParticulate</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueAirParticulate {
	<span class='added added-field ' data-is-non-breaking="">Size10 = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Size2_5 = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueAirParticulate -->
<div> <!-- start type HMCharacteristicValueAirQuality -->
<h3>New Type HomeKit.HMCharacteristicValueAirQuality</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueAirQuality {
	<span class='added added-field ' data-is-non-breaking="">Excellent = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Fair = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Good = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Inferior = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Poor = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueAirQuality -->
<div> <!-- start type HMCharacteristicValueBatteryStatus -->
<h3>New Type HomeKit.HMCharacteristicValueBatteryStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueBatteryStatus {
	<span class='added added-field ' data-is-non-breaking="">Low = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Normal = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueBatteryStatus -->
<div> <!-- start type HMCharacteristicValueCarbonDioxideDetectionStatus -->
<h3>New Type HomeKit.HMCharacteristicValueCarbonDioxideDetectionStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCarbonDioxideDetectionStatus {
	<span class='added added-field ' data-is-non-breaking="">Detected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetected = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCarbonDioxideDetectionStatus -->
<div> <!-- start type HMCharacteristicValueCarbonMonoxideDetectionStatus -->
<h3>New Type HomeKit.HMCharacteristicValueCarbonMonoxideDetectionStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCarbonMonoxideDetectionStatus {
	<span class='added added-field ' data-is-non-breaking="">Detected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetected = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCarbonMonoxideDetectionStatus -->
<div> <!-- start type HMCharacteristicValueChargingState -->
<h3>New Type HomeKit.HMCharacteristicValueChargingState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueChargingState {
	<span class='added added-field ' data-is-non-breaking="">InProgress = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueChargingState -->
<div> <!-- start type HMCharacteristicValueContactState -->
<h3>New Type HomeKit.HMCharacteristicValueContactState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueContactState {
	<span class='added added-field ' data-is-non-breaking="">Detected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueContactState -->
<div> <!-- start type HMCharacteristicValueCurrentSecuritySystemState -->
<h3>New Type HomeKit.HMCharacteristicValueCurrentSecuritySystemState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueCurrentSecuritySystemState {
	<span class='added added-field ' data-is-non-breaking="">AwayArm = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Disarmed = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NightArm = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StayArm = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Triggered = 4,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueCurrentSecuritySystemState -->
<div> <!-- start type HMCharacteristicValueDoorState -->
<h3>New Type HomeKit.HMCharacteristicValueDoorState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueDoorState {
	<span class='added added-field ' data-is-non-breaking="">Closed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Closing = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Open = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Opening = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Stopped = 4,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueDoorState -->
<div> <!-- start type HMCharacteristicValueHeatingCooling -->
<h3>New Type HomeKit.HMCharacteristicValueHeatingCooling</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueHeatingCooling {
	<span class='added added-field ' data-is-non-breaking="">Auto = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Cool = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Heat = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Off = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueHeatingCooling -->
<div> <!-- start type HMCharacteristicValueJammedStatus -->
<h3>New Type HomeKit.HMCharacteristicValueJammedStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueJammedStatus {
	<span class='added added-field ' data-is-non-breaking="">Jammed = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueJammedStatus -->
<div> <!-- start type HMCharacteristicValueLeakStatus -->
<h3>New Type HomeKit.HMCharacteristicValueLeakStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueLeakStatus {
	<span class='added added-field ' data-is-non-breaking="">Detected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueLeakStatus -->
<div> <!-- start type HMCharacteristicValueLockMechanism -->
<h3>New Type HomeKit.HMCharacteristicValueLockMechanism</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueLockMechanism {
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionSecuredRemotely = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionSecuredUsingPhysicalMovement = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionSecuredUsingPhysicalMovementExterior = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionSecuredUsingPhysicalMovementInterior = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionSecuredWithAutomaticSecureTimeout = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionSecuredWithKeypad = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionUnsecuredRemotely = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionUnsecuredUsingPhysicalMovement = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionUnsecuredUsingPhysicalMovementExterior = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionUnsecuredUsingPhysicalMovementInterior = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">LastKnownActionUnsecuredWithKeypad = 5,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueLockMechanism -->
<div> <!-- start type HMCharacteristicValueLockMechanismState -->
<h3>New Type HomeKit.HMCharacteristicValueLockMechanismState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueLockMechanismState {
	<span class='added added-field ' data-is-non-breaking="">Jammed = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Secured = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsecured = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueLockMechanismState -->
<div> <!-- start type HMCharacteristicValueOccupancyStatus -->
<h3>New Type HomeKit.HMCharacteristicValueOccupancyStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueOccupancyStatus {
	<span class='added added-field ' data-is-non-breaking="">NotOccupied = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Occupied = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueOccupancyStatus -->
<div> <!-- start type HMCharacteristicValuePositionState -->
<h3>New Type HomeKit.HMCharacteristicValuePositionState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValuePositionState {
	<span class='added added-field ' data-is-non-breaking="">Closing = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Opening = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Stopped = 2,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValuePositionState -->
<div> <!-- start type HMCharacteristicValueRotationDirection -->
<h3>New Type HomeKit.HMCharacteristicValueRotationDirection</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueRotationDirection {
	<span class='added added-field ' data-is-non-breaking="">Clockwise = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">CounterClockwise = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueRotationDirection -->
<div> <!-- start type HMCharacteristicValueSecuritySystemAlarmType -->
<h3>New Type HomeKit.HMCharacteristicValueSecuritySystemAlarmType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueSecuritySystemAlarmType {
	<span class='added added-field ' data-is-non-breaking="">NoAlarm = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueSecuritySystemAlarmType -->
<div> <!-- start type HMCharacteristicValueSmokeDetectionStatus -->
<h3>New Type HomeKit.HMCharacteristicValueSmokeDetectionStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueSmokeDetectionStatus {
	<span class='added added-field ' data-is-non-breaking="">Detected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueSmokeDetectionStatus -->
<div> <!-- start type HMCharacteristicValueStatusFault -->
<h3>New Type HomeKit.HMCharacteristicValueStatusFault</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueStatusFault {
	<span class='added added-field ' data-is-non-breaking="">GeneralFault = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NoFault = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueStatusFault -->
<div> <!-- start type HMCharacteristicValueTamperedStatus -->
<h3>New Type HomeKit.HMCharacteristicValueTamperedStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueTamperedStatus {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Tampered = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueTamperedStatus -->
<div> <!-- start type HMCharacteristicValueTargetSecuritySystemState -->
<h3>New Type HomeKit.HMCharacteristicValueTargetSecuritySystemState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueTargetSecuritySystemState {
	<span class='added added-field ' data-is-non-breaking="">AwayArm = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Disarm = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NightArm = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">StayArm = 0,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueTargetSecuritySystemState -->
<div> <!-- start type HMCharacteristicValueTemperatureUnit -->
<h3>New Type HomeKit.HMCharacteristicValueTemperatureUnit</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMCharacteristicValueTemperatureUnit {
	<span class='added added-field ' data-is-non-breaking="">Celsius = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Fahrenheit = 1,</span>
}
</pre>
</div> <!-- end type HMCharacteristicValueTemperatureUnit -->
<div> <!-- start type HMCharacteristicWriteAction -->
<h3>New Type HomeKit.HMCharacteristicWriteAction</h3>
<pre class='added' data-is-non-breaking="">
public class HMCharacteristicWriteAction : HomeKit.HMAction, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicWriteAction (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMCharacteristicWriteAction (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic Characteristic { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.INSCopying TargetValue { get; }</span>
}
</pre>
</div> <!-- end type HMCharacteristicWriteAction -->
<div> <!-- start type HMError -->
<h3>New Type HomeKit.HMError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMError {
	<span class='added added-field ' data-is-non-breaking="">AccessDenied = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryDiscoveryFailed = 57,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryIsBlocked = 61,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryIsBusy = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryNotReachable = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryOutOfCompliance = 66,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryOutOfResources = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryPairingFailed = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryPoweredOff = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessoryResponseError = 59,</span>
	<span class='added added-field ' data-is-non-breaking="">AccessorySentInvalidResponse = 50,</span>
	<span class='added added-field ' data-is-non-breaking="">ActionInAnotherActionSet = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">ActionSetExecutionFailed = 63,</span>
	<span class='added added-field ' data-is-non-breaking="">ActionSetExecutionInProgress = 65,</span>
	<span class='added added-field ' data-is-non-breaking="">ActionSetExecutionPartialSuccess = 64,</span>
	<span class='added added-field ' data-is-non-breaking="">AddAccessoryFailed = 79,</span>
	<span class='added added-field ' data-is-non-breaking="">AlreadyExists = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">BridgedAccessoryNotReachable = 88,</span>
	<span class='added added-field ' data-is-non-breaking="">CannotActivateTriggerTooFarInFuture = 71,</span>
	<span class='added added-field ' data-is-non-breaking="">CannotRemoveBuiltinActionSet = 83,</span>
	<span class='added added-field ' data-is-non-breaking="">CannotRemoveNonBridgeAccessory = 34,</span>
	<span class='added added-field ' data-is-non-breaking="">CannotUnblockNonBridgeAccessory = 81,</span>
	<span class='added added-field ' data-is-non-breaking="">ClientRequestError = 58,</span>
	<span class='added added-field ' data-is-non-breaking="">CloudDataSyncInProgress = 77,</span>
	<span class='added added-field ' data-is-non-breaking="">CommunicationFailure = 54,</span>
	<span class='added added-field ' data-is-non-breaking="">DataResetFailure = 67,</span>
	<span class='added added-field ' data-is-non-breaking="">DateMustBeOnSpecifiedBoundaries = 70,</span>
	<span class='added added-field ' data-is-non-breaking="">DeviceLocked = 82,</span>
	<span class='added added-field ' data-is-non-breaking="">FireDateInPast = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">GenericError = 52,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeAccessNotAuthorized = 47,</span>
	<span class='added added-field ' data-is-non-breaking="">HomeWithSimilarNameExists = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientPrivileges = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidAssociatedServiceType = 62,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidClass = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidDataFormatSpecified = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidMessageSize = 56,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidOrMissingAuthorizationData = 87,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidParameter = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidValueType = 43,</span>
	<span class='added added-field ' data-is-non-breaking="">KeychainSyncNotEnabled = 76,</span>
	<span class='added added-field ' data-is-non-breaking="">LocationForHomeDisabled = 84,</span>
	<span class='added added-field ' data-is-non-breaking="">MaximumObjectLimitReached = 49,</span>
	<span class='added added-field ' data-is-non-breaking="">MessageAuthenticationFailed = 55,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingEntitlement = 80,</span>
	<span class='added added-field ' data-is-non-breaking="">MissingParameter = 27,</span>
	<span class='added added-field ' data-is-non-breaking="">NameContainsProhibitedCharacters = 35,</span>
	<span class='added added-field ' data-is-non-breaking="">NameDoesNotEndWithValidCharacters = 60,</span>
	<span class='added added-field ' data-is-non-breaking="">NameDoesNotStartWithValidCharacters = 36,</span>
	<span class='added added-field ' data-is-non-breaking="">NetworkUnavailable = 78,</span>
	<span class='added added-field ' data-is-non-breaking="">NilParameter = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">NoActionsInActionSet = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">NoRegisteredActionSets = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAuthorizedForLocationServices = 85,</span>
	<span class='added added-field ' data-is-non-breaking="">NotAuthorizedForMicrophoneAccess = 89,</span>
	<span class='added added-field ' data-is-non-breaking="">NotFound = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotSignedIntoiCloud = 75,</span>
	<span class='added added-field ' data-is-non-breaking="">NotificationAlreadyEnabled = 68,</span>
	<span class='added added-field ' data-is-non-breaking="">NotificationNotSupported = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectAlreadyAssociatedToHome = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectAssociatedToAnotherHome = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectNotAssociatedToAnyHome = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">ObjectWithSimilarNameExistsInHome = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationCancelled = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationInProgress = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationNotSupported = 48,</span>
	<span class='added added-field ' data-is-non-breaking="">OperationTimedOut = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadOnlyCharacteristic = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadWriteFailure = 74,</span>
	<span class='added added-field ' data-is-non-breaking="">ReadWritePartialSuccess = 73,</span>
	<span class='added added-field ' data-is-non-breaking="">RecurrenceMustBeOnSpecifiedBoundaries = 69,</span>
	<span class='added added-field ' data-is-non-breaking="">RecurrenceTooLarge = 72,</span>
	<span class='added added-field ' data-is-non-breaking="">RecurrenceTooSmall = 42,</span>
	<span class='added added-field ' data-is-non-breaking="">ReferToUserManual = 86,</span>
	<span class='added added-field ' data-is-non-breaking="">RenameWithSimilarName = 33,</span>
	<span class='added added-field ' data-is-non-breaking="">RoomForHomeCannotBeInZone = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">RoomForHomeCannotBeUpdated = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">SecurityFailure = 53,</span>
	<span class='added added-field ' data-is-non-breaking="">StringLongerThanMaximum = 46,</span>
	<span class='added added-field ' data-is-non-breaking="">StringShorterThanMinimum = 51,</span>
	<span class='added added-field ' data-is-non-breaking="">UnconfiguredParameter = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">UserDeclinedAddingUser = 38,</span>
	<span class='added added-field ' data-is-non-breaking="">UserDeclinedInvite = 40,</span>
	<span class='added added-field ' data-is-non-breaking="">UserDeclinedRemovingUser = 39,</span>
	<span class='added added-field ' data-is-non-breaking="">UserIDNotEmailAddress = 37,</span>
	<span class='added added-field ' data-is-non-breaking="">UserManagementFailed = 41,</span>
	<span class='added added-field ' data-is-non-breaking="">ValueHigherThanMaximum = 45,</span>
	<span class='added added-field ' data-is-non-breaking="">ValueLowerThanMinimum = 44,</span>
	<span class='added added-field ' data-is-non-breaking="">WriteOnlyCharacteristic = 6,</span>
}
</pre>
</div> <!-- end type HMError -->
<div> <!-- start type HMErrors -->
<h3>New Type HomeKit.HMErrors</h3>
<pre class='added' data-is-non-breaking="">
public static class HMErrors {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString HMErrorDomain { get; }</span>
}
</pre>
</div> <!-- end type HMErrors -->
<div> <!-- start type HMEvent -->
<h3>New Type HomeKit.HMEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMEvent : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMEvent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMEvent -->
<div> <!-- start type HMEventTrigger -->
<h3>New Type HomeKit.HMEventTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class HMEventTrigger : HomeKit.HMTrigger, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMEventTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMEventTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMEvent[] Events { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTrigger (HMCharacteristic characteristic, Foundation.NSPredicateOperatorType operatorType, Foundation.NSObject value);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringAfterDate (Foundation.NSDateComponents dateComponents);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringAfterSignificantEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBeforeDate (Foundation.NSDateComponents dateComponents);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringBeforeSignificantEvent (HMSignificantEvent significantEvent, Foundation.NSDateComponents offset);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForEvaluatingTriggerOccurringOnDate (Foundation.NSDateComponents dateComponents);</span>
}
</pre>
</div> <!-- end type HMEventTrigger -->
<div> <!-- start type HMHome -->
<h3>New Type HomeKit.HMHome</h3>
<pre class='added' data-is-non-breaking="">
public class HMHome : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHome (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHome (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessory[] Accessories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMActionSet[] ActionSets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMUser CurrentUser { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IHMHomeDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Primary { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMRoom[] Rooms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMServiceGroup[] ServiceGroups { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMTrigger[] Triggers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UserFailedAccessoriesKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMZone[] Zones { get; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeAccessoryEventArgs&gt; DidAddAccessory;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeActionSetEventArgs&gt; DidAddActionSet;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeRoomEventArgs&gt; DidAddRoom;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeRoomZoneEventArgs&gt; DidAddRoomToZone;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeServiceServiceGroupEventArgs&gt; DidAddService;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeServiceGroupEventArgs&gt; DidAddServiceGroup;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeTriggerEventArgs&gt; DidAddTrigger;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeUserEventArgs&gt; DidAddUser;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeZoneEventArgs&gt; DidAddZone;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeErrorAccessoryEventArgs&gt; DidEncounterError;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeAccessoryEventArgs&gt; DidRemoveAccessory;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeActionSetEventArgs&gt; DidRemoveActionSet;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeRoomEventArgs&gt; DidRemoveRoom;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeRoomZoneEventArgs&gt; DidRemoveRoomFromZone;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeServiceServiceGroupEventArgs&gt; DidRemoveService;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeServiceGroupEventArgs&gt; DidRemoveServiceGroup;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeTriggerEventArgs&gt; DidRemoveTrigger;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeUserEventArgs&gt; DidRemoveUser;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeZoneEventArgs&gt; DidRemoveZone;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeAccessoryEventArgs&gt; DidUnblockAccessory;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeActionSetEventArgs&gt; DidUpdateActionsForActionSet;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeActionSetEventArgs&gt; DidUpdateNameForActionSet;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateNameForHome;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeRoomEventArgs&gt; DidUpdateNameForRoom;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeServiceGroupEventArgs&gt; DidUpdateNameForServiceGroup;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeTriggerEventArgs&gt; DidUpdateNameForTrigger;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeZoneEventArgs&gt; DidUpdateNameForZone;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeRoomAccessoryEventArgs&gt; DidUpdateRoom;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeTriggerEventArgs&gt; DidUpdateTrigger;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ExecuteActionSet (HMActionSet actionSet, System.Action&lt;Foundation.NSError&gt; completion);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ExecuteActionSetAsync (HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual HMActionSet GetBuiltinActionSet (string actionSetType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual HMHomeAccessControl GetHomeAccessControl (HMUser user);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual HMRoom GetRoomForEntireHome ();</span>
	<span class='added added-method ' data-is-non-breaking="">public HMService[] GetServices (HMServiceType serviceTypes);</span>
}
</pre>
</div> <!-- end type HMHome -->
<div> <!-- start type HMHomeAccessControl -->
<h3>New Type HomeKit.HMHomeAccessControl</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeAccessControl : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeAccessControl (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeAccessControl (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Administrator { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type HMHomeAccessControl -->
<div> <!-- start type HMHomeAccessoryEventArgs -->
<h3>New Type HomeKit.HMHomeAccessoryEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeAccessoryEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeAccessoryEventArgs (HMAccessory accessory);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMAccessory Accessory { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeAccessoryEventArgs -->
<div> <!-- start type HMHomeActionSetEventArgs -->
<h3>New Type HomeKit.HMHomeActionSetEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeActionSetEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeActionSetEventArgs (HMActionSet actionSet);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMActionSet ActionSet { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeActionSetEventArgs -->
<div> <!-- start type HMHomeDelegate -->
<h3>New Type HomeKit.HMHomeDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IHMHomeDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddAccessory (HMHome home, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddActionSet (HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddRoom (HMHome home, HMRoom room);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddRoomToZone (HMHome home, HMRoom room, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddService (HMHome home, HMService service, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddServiceGroup (HMHome home, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddTrigger (HMHome home, HMTrigger trigger);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddUser (HMHome home, HMUser user);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddZone (HMHome home, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEncounterError (HMHome home, Foundation.NSError error, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveAccessory (HMHome home, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveActionSet (HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveRoom (HMHome home, HMRoom room);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveRoomFromZone (HMHome home, HMRoom room, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveService (HMHome home, HMService service, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveServiceGroup (HMHome home, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveTrigger (HMHome home, HMTrigger trigger);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveUser (HMHome home, HMUser user);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveZone (HMHome home, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUnblockAccessory (HMHome home, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateActionsForActionSet (HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNameForActionSet (HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNameForHome (HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNameForRoom (HMHome home, HMRoom room);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNameForServiceGroup (HMHome home, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNameForTrigger (HMHome home, HMTrigger trigger);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateNameForZone (HMHome home, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateRoom (HMHome home, HMRoom room, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateTrigger (HMHome home, HMTrigger trigger);</span>
}
</pre>
</div> <!-- end type HMHomeDelegate -->
<div> <!-- start type HMHomeDelegate_Extensions -->
<h3>New Type HomeKit.HMHomeDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMHomeDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddAccessory (IHMHomeDelegate This, HMHome home, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddRoom (IHMHomeDelegate This, HMHome home, HMRoom room);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddRoomToZone (IHMHomeDelegate This, HMHome home, HMRoom room, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddService (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddUser (IHMHomeDelegate This, HMHome home, HMUser user);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddZone (IHMHomeDelegate This, HMHome home, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidEncounterError (IHMHomeDelegate This, HMHome home, Foundation.NSError error, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveAccessory (IHMHomeDelegate This, HMHome home, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveRoom (IHMHomeDelegate This, HMHome home, HMRoom room);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveRoomFromZone (IHMHomeDelegate This, HMHome home, HMRoom room, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveService (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveUser (IHMHomeDelegate This, HMHome home, HMUser user);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveZone (IHMHomeDelegate This, HMHome home, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUnblockAccessory (IHMHomeDelegate This, HMHome home, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateActionsForActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNameForActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNameForHome (IHMHomeDelegate This, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNameForRoom (IHMHomeDelegate This, HMHome home, HMRoom room);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNameForServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNameForTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateNameForZone (IHMHomeDelegate This, HMHome home, HMZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateRoom (IHMHomeDelegate This, HMHome home, HMRoom room, HMAccessory accessory);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);</span>
}
</pre>
</div> <!-- end type HMHomeDelegate_Extensions -->
<div> <!-- start type HMHomeErrorAccessoryEventArgs -->
<h3>New Type HomeKit.HMHomeErrorAccessoryEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeErrorAccessoryEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeErrorAccessoryEventArgs (Foundation.NSError error, HMAccessory accessory);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMAccessory Accessory { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSError Error { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeErrorAccessoryEventArgs -->
<div> <!-- start type HMHomeManager -->
<h3>New Type HomeKit.HMHomeManager</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IHMHomeManagerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMHome[] Homes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMHome PrimaryHome { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// events
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeManagerEventArgs&gt; DidAddHome;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler&lt;HMHomeManagerEventArgs&gt; DidRemoveHome;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdateHomes;</span>
	<span class='added added-event ' data-is-non-breaking="">public event System.EventHandler DidUpdatePrimaryHome;</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type HMHomeManager -->
<div> <!-- start type HMHomeManagerDelegate -->
<h3>New Type HomeKit.HMHomeManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeManagerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IHMHomeManagerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeManagerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeManagerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMHomeManagerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidAddHome (HMHomeManager manager, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidRemoveHome (HMHomeManager manager, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateHomes (HMHomeManager manager);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdatePrimaryHome (HMHomeManager manager);</span>
}
</pre>
</div> <!-- end type HMHomeManagerDelegate -->
<div> <!-- start type HMHomeManagerDelegate_Extensions -->
<h3>New Type HomeKit.HMHomeManagerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class HMHomeManagerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidAddHome (IHMHomeManagerDelegate This, HMHomeManager manager, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidRemoveHome (IHMHomeManagerDelegate This, HMHomeManager manager, HMHome home);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateHomes (IHMHomeManagerDelegate This, HMHomeManager manager);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdatePrimaryHome (IHMHomeManagerDelegate This, HMHomeManager manager);</span>
}
</pre>
</div> <!-- end type HMHomeManagerDelegate_Extensions -->
<div> <!-- start type HMHomeManagerEventArgs -->
<h3>New Type HomeKit.HMHomeManagerEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeManagerEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeManagerEventArgs (HMHome home);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMHome Home { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeManagerEventArgs -->
<div> <!-- start type HMHomeRoomAccessoryEventArgs -->
<h3>New Type HomeKit.HMHomeRoomAccessoryEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeRoomAccessoryEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeRoomAccessoryEventArgs (HMRoom room, HMAccessory accessory);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMAccessory Accessory { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HMRoom Room { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeRoomAccessoryEventArgs -->
<div> <!-- start type HMHomeRoomEventArgs -->
<h3>New Type HomeKit.HMHomeRoomEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeRoomEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeRoomEventArgs (HMRoom room);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMRoom Room { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeRoomEventArgs -->
<div> <!-- start type HMHomeRoomZoneEventArgs -->
<h3>New Type HomeKit.HMHomeRoomZoneEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeRoomZoneEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeRoomZoneEventArgs (HMRoom room, HMZone zone);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMRoom Room { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HMZone Zone { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeRoomZoneEventArgs -->
<div> <!-- start type HMHomeServiceGroupEventArgs -->
<h3>New Type HomeKit.HMHomeServiceGroupEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeServiceGroupEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeServiceGroupEventArgs (HMServiceGroup group);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMServiceGroup Group { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeServiceGroupEventArgs -->
<div> <!-- start type HMHomeServiceServiceGroupEventArgs -->
<h3>New Type HomeKit.HMHomeServiceServiceGroupEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeServiceServiceGroupEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeServiceServiceGroupEventArgs (HMService service, HMServiceGroup group);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMServiceGroup Group { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HMService Service { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeServiceServiceGroupEventArgs -->
<div> <!-- start type HMHomeTriggerEventArgs -->
<h3>New Type HomeKit.HMHomeTriggerEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeTriggerEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeTriggerEventArgs (HMTrigger trigger);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMTrigger Trigger { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeTriggerEventArgs -->
<div> <!-- start type HMHomeUserEventArgs -->
<h3>New Type HomeKit.HMHomeUserEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeUserEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeUserEventArgs (HMUser user);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMUser User { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeUserEventArgs -->
<div> <!-- start type HMHomeZoneEventArgs -->
<h3>New Type HomeKit.HMHomeZoneEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class HMHomeZoneEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMHomeZoneEventArgs (HMZone zone);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public HMZone Zone { get; set; }</span>
}
</pre>
</div> <!-- end type HMHomeZoneEventArgs -->
<div> <!-- start type HMLocationEvent -->
<h3>New Type HomeKit.HMLocationEvent</h3>
<pre class='added' data-is-non-breaking="">
public class HMLocationEvent : HomeKit.HMEvent, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMLocationEvent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMLocationEvent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLRegion Region { get; }</span>
}
</pre>
</div> <!-- end type HMLocationEvent -->
<div> <!-- start type HMRoom -->
<h3>New Type HomeKit.HMRoom</h3>
<pre class='added' data-is-non-breaking="">
public class HMRoom : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMRoom (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMRoom (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessory[] Accessories { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMRoom -->
<div> <!-- start type HMService -->
<h3>New Type HomeKit.HMService</h3>
<pre class='added' data-is-non-breaking="">
public class HMService : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public HMService ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMService (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMService (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMAccessory Accessory { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string AssociatedServiceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMCharacteristic[] Characteristics { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMService[] LinkedServices { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedDescription { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool PrimaryService { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public HMServiceType ServiceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool UserInteractive { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type HMService -->
<div> <!-- start type HMServiceGroup -->
<h3>New Type HomeKit.HMServiceGroup</h3>
<pre class='added' data-is-non-breaking="">
public class HMServiceGroup : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMServiceGroup (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMServiceGroup (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMService[] Services { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMServiceGroup -->
<div> <!-- start type HMServiceType -->
<h3>New Type HomeKit.HMServiceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum HMServiceType {
	<span class='added added-field ' data-is-non-breaking="">AccessoryInformation = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">AirQualitySensor = 10,</span>
	<span class='added added-field ' data-is-non-breaking="">Battery = 11,</span>
	<span class='added added-field ' data-is-non-breaking="">CameraControl = 29,</span>
	<span class='added added-field ' data-is-non-breaking="">CameraRtpStreamManagement = 28,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonDioxideSensor = 12,</span>
	<span class='added added-field ' data-is-non-breaking="">CarbonMonoxideSensor = 13,</span>
	<span class='added added-field ' data-is-non-breaking="">ContactSensor = 14,</span>
	<span class='added added-field ' data-is-non-breaking="">Door = 15,</span>
	<span class='added added-field ' data-is-non-breaking="">Doorbell = 32,</span>
	<span class='added added-field ' data-is-non-breaking="">Fan = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">GarageDoorOpener = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">HumiditySensor = 16,</span>
	<span class='added added-field ' data-is-non-breaking="">LeakSensor = 17,</span>
	<span class='added added-field ' data-is-non-breaking="">LightBulb = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">LightSensor = 18,</span>
	<span class='added added-field ' data-is-non-breaking="">LockManagement = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">LockMechanism = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">Microphone = 30,</span>
	<span class='added added-field ' data-is-non-breaking="">MotionSensor = 19,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OccupancySensor = 20,</span>
	<span class='added added-field ' data-is-non-breaking="">Outlet = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">SecuritySystem = 21,</span>
	<span class='added added-field ' data-is-non-breaking="">SmokeSensor = 24,</span>
	<span class='added added-field ' data-is-non-breaking="">Speaker = 31,</span>
	<span class='added added-field ' data-is-non-breaking="">StatefulProgrammableSwitch = 22,</span>
	<span class='added added-field ' data-is-non-breaking="">StatelessProgrammableSwitch = 23,</span>
	<span class='added added-field ' data-is-non-breaking="">Switch = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">TemperatureSensor = 25,</span>
	<span class='added added-field ' data-is-non-breaking="">Thermostat = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Window = 26,</span>
	<span class='added added-field ' data-is-non-breaking="">WindowCovering = 27,</span>
}
</pre>
</div> <!-- end type HMServiceType -->
<div> <!-- start type HMSignificantEvent -->
<h3>New Type HomeKit.HMSignificantEvent</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum HMSignificantEvent {
	<span class='added added-field ' data-is-non-breaking="">Sunrise = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Sunset = 1,</span>
}
</pre>
</div> <!-- end type HMSignificantEvent -->
<div> <!-- start type HMTimerTrigger -->
<h3>New Type HomeKit.HMTimerTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class HMTimerTrigger : HomeKit.HMTrigger, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimerTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTimerTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate FireDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents Recurrence { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSCalendar RecurrenceCalendar { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSTimeZone TimeZone { get; }</span>
}
</pre>
</div> <!-- end type HMTimerTrigger -->
<div> <!-- start type HMTrigger -->
<h3>New Type HomeKit.HMTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class HMTrigger : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual HMActionSet[] ActionSets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Enabled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate LastFireDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMTrigger -->
<div> <!-- start type HMUser -->
<h3>New Type HomeKit.HMUser</h3>
<pre class='added' data-is-non-breaking="">
public class HMUser : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMUser (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMUser (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMUser -->
<div> <!-- start type HMZone -->
<h3>New Type HomeKit.HMZone</h3>
<pre class='added' data-is-non-breaking="">
public class HMZone : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected HMZone (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected HMZone (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Name { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual HMRoom[] Rooms { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUuid UniqueIdentifier { get; }</span>
}
</pre>
</div> <!-- end type HMZone -->
<div> <!-- start type IHMAccessoryDelegate -->
<h3>New Type HomeKit.IHMAccessoryDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IHMAccessoryDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IHMAccessoryDelegate -->
<div> <!-- start type IHMCameraSnapshotControlDelegate -->
<h3>New Type HomeKit.IHMCameraSnapshotControlDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IHMCameraSnapshotControlDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IHMCameraSnapshotControlDelegate -->
<div> <!-- start type IHMCameraStreamControlDelegate -->
<h3>New Type HomeKit.IHMCameraStreamControlDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IHMCameraStreamControlDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IHMCameraStreamControlDelegate -->
<div> <!-- start type IHMHomeDelegate -->
<h3>New Type HomeKit.IHMHomeDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IHMHomeDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IHMHomeDelegate -->
<div> <!-- start type IHMHomeManagerDelegate -->
<h3>New Type HomeKit.IHMHomeManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IHMHomeManagerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IHMHomeManagerDelegate -->
</div> <!-- end namespace HomeKit -->

<!-- start namespace MultipeerConnectivity --> <div> 
<h2>New Namespace MultipeerConnectivity</h2>

<div> <!-- start type IMCAdvertiserAssistantDelegate -->
<h3>New Type MultipeerConnectivity.IMCAdvertiserAssistantDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IMCAdvertiserAssistantDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IMCAdvertiserAssistantDelegate -->
<div> <!-- start type IMCBrowserViewControllerDelegate -->
<h3>New Type MultipeerConnectivity.IMCBrowserViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IMCBrowserViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (MCBrowserViewController browserViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WasCancelled (MCBrowserViewController browserViewController);</span>
}
</pre>
</div> <!-- end type IMCBrowserViewControllerDelegate -->
<div> <!-- start type IMCNearbyServiceAdvertiserDelegate -->
<h3>New Type MultipeerConnectivity.IMCNearbyServiceAdvertiserDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IMCNearbyServiceAdvertiserDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveInvitationFromPeer (MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, Foundation.NSData context, MCNearbyServiceAdvertiserInvitationHandler invitationHandler);</span>
}
</pre>
</div> <!-- end type IMCNearbyServiceAdvertiserDelegate -->
<div> <!-- start type IMCNearbyServiceBrowserDelegate -->
<h3>New Type MultipeerConnectivity.IMCNearbyServiceBrowserDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IMCNearbyServiceBrowserDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, Foundation.NSDictionary info);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID);</span>
}
</pre>
</div> <!-- end type IMCNearbyServiceBrowserDelegate -->
<div> <!-- start type IMCSessionDelegate -->
<h3>New Type MultipeerConnectivity.IMCSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IMCSessionDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChangeState (MCSession session, MCPeerID peerID, MCSessionState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, Foundation.NSUrl localUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveData (MCSession session, Foundation.NSData data, MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveStream (MCSession session, Foundation.NSInputStream stream, string streamName, MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, Foundation.NSProgress progress);</span>
}
</pre>
</div> <!-- end type IMCSessionDelegate -->
<div> <!-- start type MCAdvertiserAssistant -->
<h3>New Type MultipeerConnectivity.MCAdvertiserAssistant</h3>
<pre class='added' data-is-non-breaking="">
public class MCAdvertiserAssistant : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCAdvertiserAssistant (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCAdvertiserAssistant (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCAdvertiserAssistant (string serviceType, Foundation.NSDictionary info, MCSession session);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IMCAdvertiserAssistantDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary DiscoveryInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ServiceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MCSession Session { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Start ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Stop ();</span>
}
</pre>
</div> <!-- end type MCAdvertiserAssistant -->
<div> <!-- start type MCAdvertiserAssistantDelegate -->
<h3>New Type MultipeerConnectivity.MCAdvertiserAssistantDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class MCAdvertiserAssistantDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IMCAdvertiserAssistantDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MCAdvertiserAssistantDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCAdvertiserAssistantDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCAdvertiserAssistantDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidDismissInvitation (MCAdvertiserAssistant advertiserAssistant);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillPresentInvitation (MCAdvertiserAssistant advertiserAssistant);</span>
}
</pre>
</div> <!-- end type MCAdvertiserAssistantDelegate -->
<div> <!-- start type MCAdvertiserAssistantDelegate_Extensions -->
<h3>New Type MultipeerConnectivity.MCAdvertiserAssistantDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MCAdvertiserAssistantDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidDismissInvitation (IMCAdvertiserAssistantDelegate This, MCAdvertiserAssistant advertiserAssistant);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillPresentInvitation (IMCAdvertiserAssistantDelegate This, MCAdvertiserAssistant advertiserAssistant);</span>
}
</pre>
</div> <!-- end type MCAdvertiserAssistantDelegate_Extensions -->
<div> <!-- start type MCBrowserViewController -->
<h3>New Type MultipeerConnectivity.MCBrowserViewController</h3>
<pre class='added' data-is-non-breaking="">
public class MCBrowserViewController : UIKit.UIViewController, Foundation.INSCoding, Foundation.INSObjectProtocol, IMCNearbyServiceBrowserDelegate, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MCBrowserViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCBrowserViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCBrowserViewController (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCBrowserViewController (MCNearbyServiceBrowser browser, MCSession session);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCBrowserViewController (string nibName, Foundation.NSBundle bundle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCBrowserViewController (string serviceType, MCSession session);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual MCNearbyServiceBrowser Browser { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IMCBrowserViewControllerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MaximumNumberOfPeers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint MinimumNumberOfPeers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MCSession Session { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidNotStartBrowsingForPeers (MCNearbyServiceBrowser browser, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, Foundation.NSDictionary info);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID);</span>
}
</pre>
</div> <!-- end type MCBrowserViewController -->
<div> <!-- start type MCBrowserViewControllerDelegate -->
<h3>New Type MultipeerConnectivity.MCBrowserViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MCBrowserViewControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IMCBrowserViewControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCBrowserViewControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCBrowserViewControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCBrowserViewControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (MCBrowserViewController browserViewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool ShouldPresentNearbyPeer (MCBrowserViewController browserViewController, MCPeerID peerID, Foundation.NSDictionary info);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WasCancelled (MCBrowserViewController browserViewController);</span>
}
</pre>
</div> <!-- end type MCBrowserViewControllerDelegate -->
<div> <!-- start type MCBrowserViewControllerDelegate_Extensions -->
<h3>New Type MultipeerConnectivity.MCBrowserViewControllerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MCBrowserViewControllerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool ShouldPresentNearbyPeer (IMCBrowserViewControllerDelegate This, MCBrowserViewController browserViewController, MCPeerID peerID, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type MCBrowserViewControllerDelegate_Extensions -->
<div> <!-- start type MCEncryptionPreference -->
<h3>New Type MultipeerConnectivity.MCEncryptionPreference</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MCEncryptionPreference {
	<span class='added added-field ' data-is-non-breaking="">None = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Optional = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Required = 1,</span>
}
</pre>
</div> <!-- end type MCEncryptionPreference -->
<div> <!-- start type MCError -->
<h3>New Type MultipeerConnectivity.MCError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MCError {
	<span class='added added-field ' data-is-non-breaking="">Cancelled = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidParameter = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotConnected = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">TimedOut = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Unavailable = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unsupported = 3,</span>
}
</pre>
</div> <!-- end type MCError -->
<div> <!-- start type MCErrorExtensions -->
<h3>New Type MultipeerConnectivity.MCErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MCErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (MCError self);</span>
}
</pre>
</div> <!-- end type MCErrorExtensions -->
<div> <!-- start type MCNearbyServiceAdvertiser -->
<h3>New Type MultipeerConnectivity.MCNearbyServiceAdvertiser</h3>
<pre class='added' data-is-non-breaking="">
public class MCNearbyServiceAdvertiser : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceAdvertiser (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceAdvertiser (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCNearbyServiceAdvertiser (MCPeerID myPeerID, Foundation.NSDictionary info, string serviceType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IMCNearbyServiceAdvertiserDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary DiscoveryInfo { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MCPeerID MyPeerID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ServiceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartAdvertisingPeer ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopAdvertisingPeer ();</span>
}
</pre>
</div> <!-- end type MCNearbyServiceAdvertiser -->
<div> <!-- start type MCNearbyServiceAdvertiserDelegate -->
<h3>New Type MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MCNearbyServiceAdvertiserDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IMCNearbyServiceAdvertiserDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceAdvertiserDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceAdvertiserDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceAdvertiserDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidNotStartAdvertisingPeer (MCNearbyServiceAdvertiser advertiser, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveInvitationFromPeer (MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, Foundation.NSData context, MCNearbyServiceAdvertiserInvitationHandler invitationHandler);</span>
}
</pre>
</div> <!-- end type MCNearbyServiceAdvertiserDelegate -->
<div> <!-- start type MCNearbyServiceAdvertiserDelegate_Extensions -->
<h3>New Type MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MCNearbyServiceAdvertiserDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidNotStartAdvertisingPeer (IMCNearbyServiceAdvertiserDelegate This, MCNearbyServiceAdvertiser advertiser, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MCNearbyServiceAdvertiserDelegate_Extensions -->
<div> <!-- start type MCNearbyServiceAdvertiserInvitationHandler -->
<h3>New Type MultipeerConnectivity.MCNearbyServiceAdvertiserInvitationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MCNearbyServiceAdvertiserInvitationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MCNearbyServiceAdvertiserInvitationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (bool accept, MCSession session, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (bool accept, MCSession session);</span>
}
</pre>
</div> <!-- end type MCNearbyServiceAdvertiserInvitationHandler -->
<div> <!-- start type MCNearbyServiceBrowser -->
<h3>New Type MultipeerConnectivity.MCNearbyServiceBrowser</h3>
<pre class='added' data-is-non-breaking="">
public class MCNearbyServiceBrowser : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceBrowser (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceBrowser (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCNearbyServiceBrowser (MCPeerID myPeerID, string serviceType);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IMCNearbyServiceBrowserDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MCPeerID MyPeerID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ServiceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InvitePeer (MCPeerID peerID, MCSession session, Foundation.NSData context, double timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartBrowsingForPeers ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopBrowsingForPeers ();</span>
}
</pre>
</div> <!-- end type MCNearbyServiceBrowser -->
<div> <!-- start type MCNearbyServiceBrowserDelegate -->
<h3>New Type MultipeerConnectivity.MCNearbyServiceBrowserDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MCNearbyServiceBrowserDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IMCNearbyServiceBrowserDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceBrowserDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceBrowserDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCNearbyServiceBrowserDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidNotStartBrowsingForPeers (MCNearbyServiceBrowser browser, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, Foundation.NSDictionary info);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID);</span>
}
</pre>
</div> <!-- end type MCNearbyServiceBrowserDelegate -->
<div> <!-- start type MCNearbyServiceBrowserDelegate_Extensions -->
<h3>New Type MultipeerConnectivity.MCNearbyServiceBrowserDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MCNearbyServiceBrowserDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidNotStartBrowsingForPeers (IMCNearbyServiceBrowserDelegate This, MCNearbyServiceBrowser browser, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MCNearbyServiceBrowserDelegate_Extensions -->
<div> <!-- start type MCPeerID -->
<h3>New Type MultipeerConnectivity.MCPeerID</h3>
<pre class='added' data-is-non-breaking="">
public class MCPeerID : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MCPeerID (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCPeerID (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCPeerID (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCPeerID (string myDisplayName);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string DisplayName { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type MCPeerID -->
<div> <!-- start type MCSession -->
<h3>New Type MultipeerConnectivity.MCSession</h3>
<pre class='added' data-is-non-breaking="">
public class MCSession : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCSession (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCSession (MCPeerID myPeerID);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCSession (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCSession (MCPeerID myPeerID, Security.SecIdentity identity, MCEncryptionPreference encryptionPreference);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public MCSession (MCPeerID myPeerID, Security.SecIdentity identity, Security.SecCertificate[] certificates, MCEncryptionPreference encryptionPreference);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MCPeerID[] ConnectedPeers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IMCSessionDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MCEncryptionPreference EncryptionPreference { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static nint MaximumNumberOfPeers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static nint MinimumNumberOfPeers { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual MCPeerID MyPeerID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSArray SecurityIdentity { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelConnectPeer (MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ConnectPeer (MCPeerID peerID, Foundation.NSData data);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Disconnect ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void NearbyConnectionDataForPeer (MCPeerID peerID, MCSessionNearbyConnectionDataForPeerCompletionHandler completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool SendData (Foundation.NSData data, MCPeerID[] peerIDs, MCSessionSendDataMode mode, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSProgress SendResource (Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSOutputStream StartStream (string streamName, MCPeerID peerID, out Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MCSession -->
<div> <!-- start type MCSessionDelegate -->
<h3>New Type MultipeerConnectivity.MCSessionDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class MCSessionDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, IMCSessionDelegate, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected MCSessionDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCSessionDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected MCSessionDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChangeState (MCSession session, MCPeerID peerID, MCSessionState state);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, Foundation.NSUrl localUrl, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool DidReceiveCertificate (MCSession session, Security.SecCertificate[] certificate, MCPeerID peerID, System.Action&lt;bool&gt; certificateHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveData (MCSession session, Foundation.NSData data, MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidReceiveStream (MCSession session, Foundation.NSInputStream stream, string streamName, MCPeerID peerID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, Foundation.NSProgress progress);</span>
}
</pre>
</div> <!-- end type MCSessionDelegate -->
<div> <!-- start type MCSessionDelegate_Extensions -->
<h3>New Type MultipeerConnectivity.MCSessionDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class MCSessionDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static bool DidReceiveCertificate (IMCSessionDelegate This, MCSession session, Security.SecCertificate[] certificate, MCPeerID peerID, System.Action&lt;bool&gt; certificateHandler);</span>
}
</pre>
</div> <!-- end type MCSessionDelegate_Extensions -->
<div> <!-- start type MCSessionNearbyConnectionDataForPeerCompletionHandler -->
<h3>New Type MultipeerConnectivity.MCSessionNearbyConnectionDataForPeerCompletionHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate MCSessionNearbyConnectionDataForPeerCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public MCSessionNearbyConnectionDataForPeerCompletionHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData connectionData, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData connectionData, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type MCSessionNearbyConnectionDataForPeerCompletionHandler -->
<div> <!-- start type MCSessionSendDataMode -->
<h3>New Type MultipeerConnectivity.MCSessionSendDataMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MCSessionSendDataMode {
	<span class='added added-field ' data-is-non-breaking="">Reliable = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Unreliable = 1,</span>
}
</pre>
</div> <!-- end type MCSessionSendDataMode -->
<div> <!-- start type MCSessionState -->
<h3>New Type MultipeerConnectivity.MCSessionState</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum MCSessionState {
	<span class='added added-field ' data-is-non-breaking="">Connected = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Connecting = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotConnected = 0,</span>
}
</pre>
</div> <!-- end type MCSessionState -->
</div> <!-- end namespace MultipeerConnectivity -->

<!-- start namespace Photos --> <div> 
<h2>New Namespace Photos</h2>

<div> <!-- start type IPHLivePhotoFrame -->
<h3>New Type Photos.IPHLivePhotoFrame</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHLivePhotoFrame : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIImage Image { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nfloat RenderScale { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime Time { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhotoFrameType Type { get; }</span>
}
</pre>
</div> <!-- end type IPHLivePhotoFrame -->
<div> <!-- start type IPHPhotoLibraryChangeObserver -->
<h3>New Type Photos.IPHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHPhotoLibraryChangeObserver : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type IPHPhotoLibraryChangeObserver -->
<div> <!-- start type PHAdjustmentData -->
<h3>New Type Photos.PHAdjustmentData</h3>
<pre class='added' data-is-non-breaking="">
public class PHAdjustmentData : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAdjustmentData ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHAdjustmentData (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAdjustmentData (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAdjustmentData (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHAdjustmentData (string formatIdentifier, string formatVersion, Foundation.NSData data);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData Data { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FormatIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string FormatVersion { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHAdjustmentData -->
<div> <!-- start type PHAsset -->
<h3>New Type Photos.PHAsset</h3>
<pre class='added' data-is-non-breaking="">
public class PHAsset : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAsset ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAsset (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string BurstIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetBurstSelectionType BurstSelectionTypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Favorite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaSubtype MediaSubtypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaType MediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate ModificationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelHeight { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint PixelWidth { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool RepresentsBurst { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType SourceType { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHAssetEditOperation editOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (Foundation.NSUrl[] assetUrls, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (PHAssetMediaType mediaType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssets (string burstIdentifier, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetsUsingLocalIdentifiers (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchKeyAssets (PHAssetCollection assetCollection, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHAsset -->
<div> <!-- start type PHAssetBurstSelectionType -->
<h3>New Type Photos.PHAssetBurstSelectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PHAssetBurstSelectionType {
	<span class='added added-field ' data-is-non-breaking="">AutoPick = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserPick = 2,</span>
}
</pre>
</div> <!-- end type PHAssetBurstSelectionType -->
<div> <!-- start type PHAssetChangeRequest -->
<h3>New Type Photos.PHAssetChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetChangeRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHContentEditingOutput ContentEditingOutput { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Favorite { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Hidden { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObjectPlaceholder PlaceholderForCreatedAsset { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetChangeRequest ChangeRequest (PHAsset asset);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteAssets (PHAsset[] assets);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetChangeRequest FromImage (Foundation.NSUrl fileUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetChangeRequest FromImage (UIKit.UIImage image);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetChangeRequest FromVideo (Foundation.NSUrl fileUrl);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RevertAssetContentToOriginal ();</span>
}
</pre>
</div> <!-- end type PHAssetChangeRequest -->
<div> <!-- start type PHAssetCollection -->
<h3>New Type Photos.PHAssetCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetCollection : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetCollection ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation ApproximateLocation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionSubtype AssetCollectionSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetCollectionType AssetCollectionType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint EstimatedAssetCount { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (Foundation.NSUrl[] assetGroupUrls, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAsset asset, PHAssetCollectionType type, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchAssetCollections (PHAssetCollectionType type, PHAssetCollectionSubtype subtype, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMoments (PHCollectionList momentList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHAsset[] assets, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollection GetTransientAssetCollection (PHFetchResult fetchResult, string title);</span>
}
</pre>
</div> <!-- end type PHAssetCollection -->
<div> <!-- start type PHAssetCollectionChangeRequest -->
<h3>New Type Photos.PHAssetCollectionChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetCollectionChangeRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollectionChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCollectionChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObjectPlaceholder PlaceholderForCreatedAssetCollection { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddAssets (PHObject[] assets);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollectionChangeRequest ChangeRequest (PHAssetCollection assetCollection);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollectionChangeRequest ChangeRequest (PHAssetCollection assetCollection, PHFetchResult assets);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCollectionChangeRequest CreateAssetCollection (string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteAssetCollections (PHAssetCollection[] assetCollections);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InsertAssets (PHObject[] assets, Foundation.NSIndexSet indexes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MoveAssets (Foundation.NSIndexSet fromIndexes, uint toIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAssets (Foundation.NSIndexSet indexes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAssets (PHObject[] assets);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReplaceAssets (Foundation.NSIndexSet indexes, PHObject[] assets);</span>
}
</pre>
</div> <!-- end type PHAssetCollectionChangeRequest -->
<div> <!-- start type PHAssetCollectionSubtype -->
<h3>New Type Photos.PHAssetCollectionSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetCollectionSubtype {
	<span class='added added-field ' data-is-non-breaking="">AlbumCloudShared = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumImported = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumMyPhotoStream = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumRegular = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumSyncedAlbum = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumSyncedEvent = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">AlbumSyncedFaces = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Any = 9223372036854775807,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumAllHidden = 205,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumBursts = 207,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumFavorites = 203,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumGeneric = 200,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumPanoramas = 201,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumRecentlyAdded = 206,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumScreenshots = 211,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumSelfPortraits = 210,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumSlomoVideos = 208,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumTimelapses = 204,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumUserLibrary = 209,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbumVideos = 202,</span>
}
</pre>
</div> <!-- end type PHAssetCollectionSubtype -->
<div> <!-- start type PHAssetCollectionType -->
<h3>New Type Photos.PHAssetCollectionType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetCollectionType {
	<span class='added added-field ' data-is-non-breaking="">Album = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Moment = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartAlbum = 2,</span>
}
</pre>
</div> <!-- end type PHAssetCollectionType -->
<div> <!-- start type PHAssetContentEditingInputExtensions -->
<h3>New Type Photos.PHAssetContentEditingInputExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PHAssetContentEditingInputExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelContentEditingInputRequest (PHAsset This, uint requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public static uint RequestContentEditingInput (PHAsset This, PHContentEditingInputRequestOptions options, PHContentEditingHandler completionHandler);</span>
}
</pre>
</div> <!-- end type PHAssetContentEditingInputExtensions -->
<div> <!-- start type PHAssetCreationRequest -->
<h3>New Type Photos.PHAssetCreationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetCreationRequest : Photos.PHAssetChangeRequest, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCreationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetCreationRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddResource (PHAssetResourceType type, Foundation.NSData data, PHAssetResourceCreationOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddResource (PHAssetResourceType type, Foundation.NSUrl fileURL, PHAssetResourceCreationOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetCreationRequest CreationRequestForAsset ();</span>
	<span class='added added-method ' data-is-non-breaking="">public bool SupportsAssetResourceTypes (PHAssetResourceType[] resourceTypes);</span>
}
</pre>
</div> <!-- end type PHAssetCreationRequest -->
<div> <!-- start type PHAssetEditOperation -->
<h3>New Type Photos.PHAssetEditOperation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetEditOperation {
	<span class='added added-field ' data-is-non-breaking="">Content = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Delete = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Properties = 3,</span>
}
</pre>
</div> <!-- end type PHAssetEditOperation -->
<div> <!-- start type PHAssetImageProgressHandler -->
<h3>New Type Photos.PHAssetImageProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHAssetImageProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetImageProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (double progress, Foundation.NSError error, out bool stop, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (out bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (double progress, Foundation.NSError error, out bool stop, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHAssetImageProgressHandler -->
<div> <!-- start type PHAssetMediaSubtype -->
<h3>New Type Photos.PHAssetMediaSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PHAssetMediaSubtype {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">PhotoHDR = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">PhotoLive = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">PhotoPanorama = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Screenshot = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoHighFrameRate = 131072,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoStreamed = 65536,</span>
	<span class='added added-field ' data-is-non-breaking="">VideoTimelapse = 262144,</span>
}
</pre>
</div> <!-- end type PHAssetMediaSubtype -->
<div> <!-- start type PHAssetMediaType -->
<h3>New Type Photos.PHAssetMediaType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetMediaType {
	<span class='added added-field ' data-is-non-breaking="">Audio = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Image = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type PHAssetMediaType -->
<div> <!-- start type PHAssetResource -->
<h3>New Type Photos.PHAssetResource</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetResource : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResource (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResource (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AssetLocalIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string OriginalFilename { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetResourceType ResourceType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string UniformTypeIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetResource[] GetAssetResources (PHAsset forAsset);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHAssetResource[] GetAssetResources (PHLivePhoto livePhoto);</span>
}
</pre>
</div> <!-- end type PHAssetResource -->
<div> <!-- start type PHAssetResourceCreationOptions -->
<h3>New Type Photos.PHAssetResourceCreationOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetResourceCreationOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetResourceCreationOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResourceCreationOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResourceCreationOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string OriginalFilename { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ShouldMoveFile { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string UniformTypeIdentifier { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHAssetResourceCreationOptions -->
<div> <!-- start type PHAssetResourceManager -->
<h3>New Type Photos.PHAssetResourceManager</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetResourceManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResourceManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResourceManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHAssetResourceManager DefaultManager { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelDataRequest (int requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestData (PHAssetResource forResource, PHAssetResourceRequestOptions options, System.Action&lt;Foundation.NSData&gt; handler, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WriteData (PHAssetResource forResource, Foundation.NSUrl fileURL, PHAssetResourceRequestOptions options, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
}
</pre>
</div> <!-- end type PHAssetResourceManager -->
<div> <!-- start type PHAssetResourceRequestOptions -->
<h3>New Type Photos.PHAssetResourceRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHAssetResourceRequestOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetResourceRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResourceRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHAssetResourceRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Action&lt;double&gt; ProgressHandler { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHAssetResourceRequestOptions -->
<div> <!-- start type PHAssetResourceType -->
<h3>New Type Photos.PHAssetResourceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetResourceType {
	<span class='added added-field ' data-is-non-breaking="">AdjustmentBasePhoto = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">AdjustmentData = 7,</span>
	<span class='added added-field ' data-is-non-breaking="">AlternatePhoto = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Audio = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">FullSizePhoto = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">FullSizeVideo = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">PairedVideo = 9,</span>
	<span class='added added-field ' data-is-non-breaking="">Photo = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 2,</span>
}
</pre>
</div> <!-- end type PHAssetResourceType -->
<div> <!-- start type PHAssetSourceType -->
<h3>New Type Photos.PHAssetSourceType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAssetSourceType {
	<span class='added added-field ' data-is-non-breaking="">CloudShared = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">UserLibrary = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">iTunesSynced = 4,</span>
}
</pre>
</div> <!-- end type PHAssetSourceType -->
<div> <!-- start type PHAssetVideoProgressHandler -->
<h3>New Type Photos.PHAssetVideoProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHAssetVideoProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHAssetVideoProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (double progress, Foundation.NSError error, out bool stop, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (out bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (double progress, Foundation.NSError error, out bool stop, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHAssetVideoProgressHandler -->
<div> <!-- start type PHAuthorizationStatus -->
<h3>New Type Photos.PHAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type PHAuthorizationStatus -->
<div> <!-- start type PHCachingImageManager -->
<h3>New Type Photos.PHCachingImageManager</h3>
<pre class='added' data-is-non-breaking="">
public class PHCachingImageManager : Photos.PHImageManager, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCachingImageManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCachingImageManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCachingImageManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AllowsCachingHighQualityImages { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartCaching (PHAsset[] assets, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHImageRequestOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopCaching ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopCaching (PHAsset[] assets, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHImageRequestOptions options);</span>
}
</pre>
</div> <!-- end type PHCachingImageManager -->
<div> <!-- start type PHChange -->
<h3>New Type Photos.PHChange</h3>
<pre class='added' data-is-non-breaking="">
public class PHChange : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChange ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHChange (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual PHFetchResultChangeDetails GetFetchResultChangeDetails (PHFetchResult obj);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual PHObjectChangeDetails GetObjectChangeDetails (PHObject obj);</span>
}
</pre>
</div> <!-- end type PHChange -->
<div> <!-- start type PHChangeDetailEnumerator -->
<h3>New Type Photos.PHChangeDetailEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHChangeDetailEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHChangeDetailEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (uint fromIndex, uint toIndex, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (uint fromIndex, uint toIndex);</span>
}
</pre>
</div> <!-- end type PHChangeDetailEnumerator -->
<div> <!-- start type PHCollection -->
<h3>New Type Photos.PHCollection</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollection : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollection (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainAssets { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool CanContainCollections { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedTitle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool CanPerformEditOperation (PHCollectionEditOperation anOperation);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollections (PHCollectionList collectionList, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchTopLevelUserCollections (PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollection -->
<div> <!-- start type PHCollectionEditOperation -->
<h3>New Type Photos.PHCollectionEditOperation</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHCollectionEditOperation {
	<span class='added added-field ' data-is-non-breaking="">AddContent = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">CreateContent = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Delete = 6,</span>
	<span class='added added-field ' data-is-non-breaking="">DeleteContent = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">RearrangeContent = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">RemoveContent = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Rename = 7,</span>
}
</pre>
</div> <!-- end type PHCollectionEditOperation -->
<div> <!-- start type PHCollectionList -->
<h3>New Type Photos.PHCollectionList</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollectionList : Photos.PHCollection, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHCollectionList ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionList (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListSubtype CollectionListSubtype { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHCollectionListType CollectionListType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate EndDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] LocalizedLocationNames { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate StartDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHAssetCollection[] collections, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionList CreateTransientCollectionList (PHFetchResult fetchResult, string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollection collection, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (string[] identifiers, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchCollectionLists (PHCollectionListType type, PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHFetchOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHAssetCollection moment, PHFetchOptions options);</span>
}
</pre>
</div> <!-- end type PHCollectionList -->
<div> <!-- start type PHCollectionListChangeRequest -->
<h3>New Type Photos.PHCollectionListChangeRequest</h3>
<pre class='added' data-is-non-breaking="">
public class PHCollectionListChangeRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionListChangeRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHCollectionListChangeRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObjectPlaceholder PlaceholderForCreatedCollectionList { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Title { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddChildCollections (PHCollection[] collections);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionListChangeRequest ChangeRequest (PHCollectionList collectionList);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionListChangeRequest ChangeRequest (PHCollectionList collectionList, PHFetchResult childCollections);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHCollectionListChangeRequest CreateAssetCollection (string title);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DeleteCollectionLists (PHCollectionList[] collectionLists);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void InsertChildCollections (PHCollection[] collections, Foundation.NSIndexSet indexes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void MoveChildCollections (Foundation.NSIndexSet indexes, uint toIndex);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveChildCollections (Foundation.NSIndexSet indexes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveChildCollections (PHCollection[] collections);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ReplaceChildCollection (Foundation.NSIndexSet indexes, PHCollection[] collections);</span>
}
</pre>
</div> <!-- end type PHCollectionListChangeRequest -->
<div> <!-- start type PHCollectionListSubtype -->
<h3>New Type Photos.PHCollectionListSubtype</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHCollectionListSubtype {
	<span class='added added-field ' data-is-non-breaking="">Any = 9223372036854775807,</span>
	<span class='added added-field ' data-is-non-breaking="">MomentListCluster = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MomentListYear = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">RegularFolder = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartFolderEvents = 200,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartFolderFaces = 201,</span>
}
</pre>
</div> <!-- end type PHCollectionListSubtype -->
<div> <!-- start type PHCollectionListType -->
<h3>New Type Photos.PHCollectionListType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHCollectionListType {
	<span class='added added-field ' data-is-non-breaking="">Folder = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">MomentList = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">SmartFolder = 3,</span>
}
</pre>
</div> <!-- end type PHCollectionListType -->
<div> <!-- start type PHContentEditingHandler -->
<h3>New Type Photos.PHContentEditingHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHContentEditingHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (PHContentEditingInput contentEditingInput, Foundation.NSDictionary requestStatusInfo, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (PHContentEditingInput contentEditingInput, Foundation.NSDictionary requestStatusInfo);</span>
}
</pre>
</div> <!-- end type PHContentEditingHandler -->
<div> <!-- start type PHContentEditingInput -->
<h3>New Type Photos.PHContentEditingInput</h3>
<pre class='added' data-is-non-breaking="">
public class PHContentEditingInput : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingInput ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingInput (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingInput (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAdjustmentData AdjustmentData { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVAsset AudiovisualAsset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual AVFoundation.AVAsset AvAsset { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate CreationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIImage DisplaySizeImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIImageOrientation FullSizeImageOrientation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl FullSizeImageUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhoto LivePhoto { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreLocation.CLLocation Location { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaSubtype MediaSubtypes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetMediaType MediaType { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string UniformTypeIdentifier { get; }</span>
}
</pre>
</div> <!-- end type PHContentEditingInput -->
<div> <!-- start type PHContentEditingInputRequestOptions -->
<h3>New Type Photos.PHContentEditingInputRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHContentEditingInputRequestOptions : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingInputRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingInputRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingInputRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual System.Func&lt;PHAdjustmentData,System.Boolean&gt; CanHandleAdjustmentData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CancelledKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString InputErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsInCloudKey { get; }</span>
}
</pre>
</div> <!-- end type PHContentEditingInputRequestOptions -->
<div> <!-- start type PHContentEditingOutput -->
<h3>New Type Photos.PHContentEditingOutput</h3>
<pre class='added' data-is-non-breaking="">
public class PHContentEditingOutput : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingOutput ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingOutput (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingOutput (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingOutput (PHContentEditingInput contentEditingInput);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHContentEditingOutput (PHObjectPlaceholder placeholderForCreatedAsset);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHContentEditingOutput (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAdjustmentData AdjustmentData { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl RenderedContentUrl { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type PHContentEditingOutput -->
<div> <!-- start type PHFetchOptions -->
<h3>New Type Photos.PHFetchOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual uint FetchLimit { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeAllBurstAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetSourceType IncludeAssetSourceTypes { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeHiddenAssets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSPredicate Predicate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSSortDescriptor[] SortDescriptors { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool WantsIncrementalChangeDetails { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHFetchOptions -->
<div> <!-- start type PHFetchResult -->
<h3>New Type Photos.PHFetchResult</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResult : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.Generic.IEnumerable&lt;Foundation.NSObject&gt;, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual nint Count { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSObject Item { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject LastObject { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject firstObject { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual bool Contains (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual uint CountOfAssetsWithMediaType (PHAssetMediaType mediaType);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Enumerate (Foundation.NSIndexSet idx, Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Collections.Generic.IEnumerator&lt;Foundation.NSObject&gt; GetEnumerator ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual nint IndexOf (Foundation.NSObject id, Foundation.NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAt (nint index);</span>
	<span class='added added-method ' data-is-non-breaking="">public T[] ObjectsAt&lt;T&gt; (Foundation.NSIndexSet indexes);</span>
}
</pre>
</div> <!-- end type PHFetchResult -->
<div> <!-- start type PHFetchResultChangeDetails -->
<h3>New Type Photos.PHFetchResultChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHFetchResultChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHFetchResultChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet ChangedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] ChangedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHFetchResult FetchResultBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasIncrementalChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool HasMoves { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet InsertedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] InsertedObjects { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSIndexSet RemovedIndexes { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHObject[] RemovedObjects { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHFetchResultChangeDetails ChangeDetails (PHFetchResult fromResult, PHFetchResult toResult, PHObject[] changedObjects);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EnumerateMoves (PHChangeDetailEnumerator handler);</span>
}
</pre>
</div> <!-- end type PHFetchResultChangeDetails -->
<div> <!-- start type PHFetchResultEnumerator -->
<h3>New Type Photos.PHFetchResultEnumerator</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHFetchResultEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHFetchResultEnumerator (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject element, uint elementIndex, out bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (out bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSObject element, uint elementIndex, out bool stop);</span>
}
</pre>
</div> <!-- end type PHFetchResultEnumerator -->
<div> <!-- start type PHImageContentMode -->
<h3>New Type Photos.PHImageContentMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageContentMode {
	<span class='added added-field ' data-is-non-breaking="">AspectFill = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">AspectFit = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Default = 0,</span>
}
</pre>
</div> <!-- end type PHImageContentMode -->
<div> <!-- start type PHImageDataHandler -->
<h3>New Type Photos.PHImageDataHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageDataHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (Foundation.NSData data, Foundation.NSString dataUti, UIKit.UIImageOrientation orientation, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (Foundation.NSData data, Foundation.NSString dataUti, UIKit.UIImageOrientation orientation, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageDataHandler -->
<div> <!-- start type PHImageKeys -->
<h3>New Type Photos.PHImageKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class PHImageKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Cancelled { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString Error { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsDegraded { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultIsInCloud { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ResultRequestID { get; }</span>
}
</pre>
</div> <!-- end type PHImageKeys -->
<div> <!-- start type PHImageManager -->
<h3>New Type Photos.PHImageManager</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHImageManager DefaultManager { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CoreGraphics.CGSize MaximumSize { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CancelImageRequest (int requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestAvAsset (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestAvAssetHandler resultHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestExportSession (PHAsset asset, PHVideoRequestOptions options, string exportPreset, PHImageManagerRequestExportHandler resultHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageData (PHAsset asset, PHImageRequestOptions options, PHImageDataHandler handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestImageForAsset (PHAsset asset, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestLivePhoto (PHAsset asset, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, PHLivePhotoRequestOptions options, PHImageManagerRequestLivePhoto resultHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual int RequestPlayerItem (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestPlayerHandler resultHandler);</span>
}
</pre>
</div> <!-- end type PHImageManager -->
<div> <!-- start type PHImageManagerRequestAvAssetHandler -->
<h3>New Type Photos.PHImageManagerRequestAvAssetHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageManagerRequestAvAssetHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManagerRequestAvAssetHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AVFoundation.AVAsset asset, AVFoundation.AVAudioMix audioMix, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (AVFoundation.AVAsset asset, AVFoundation.AVAudioMix audioMix, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageManagerRequestAvAssetHandler -->
<div> <!-- start type PHImageManagerRequestExportHandler -->
<h3>New Type Photos.PHImageManagerRequestExportHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageManagerRequestExportHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManagerRequestExportHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AVFoundation.AVAssetExportSession exportSession, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (AVFoundation.AVAssetExportSession exportSession, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageManagerRequestExportHandler -->
<div> <!-- start type PHImageManagerRequestLivePhoto -->
<h3>New Type Photos.PHImageManagerRequestLivePhoto</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageManagerRequestLivePhoto : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManagerRequestLivePhoto (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (PHLivePhoto livePhoto, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (PHLivePhoto livePhoto, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageManagerRequestLivePhoto -->
<div> <!-- start type PHImageManagerRequestPlayerHandler -->
<h3>New Type Photos.PHImageManagerRequestPlayerHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageManagerRequestPlayerHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageManagerRequestPlayerHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (AVFoundation.AVPlayerItem playerItem, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (AVFoundation.AVPlayerItem playerItem, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageManagerRequestPlayerHandler -->
<div> <!-- start type PHImageRequestOptions -->
<h3>New Type Photos.PHImageRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHImageRequestOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHImageRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGRect NormalizedCropRect { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsResizeMode ResizeMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Synchronous { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsVersion Version { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHImageRequestOptions -->
<div> <!-- start type PHImageRequestOptionsDeliveryMode -->
<h3>New Type Photos.PHImageRequestOptionsDeliveryMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsDeliveryMode {
	<span class='added added-field ' data-is-non-breaking="">FastFormat = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">HighQualityFormat = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Opportunistic = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsDeliveryMode -->
<div> <!-- start type PHImageRequestOptionsResizeMode -->
<h3>New Type Photos.PHImageRequestOptionsResizeMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsResizeMode {
	<span class='added added-field ' data-is-non-breaking="">Exact = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Fast = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsResizeMode -->
<div> <!-- start type PHImageRequestOptionsVersion -->
<h3>New Type Photos.PHImageRequestOptionsVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHImageRequestOptionsVersion {
	<span class='added added-field ' data-is-non-breaking="">Current = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Original = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Unadjusted = 1,</span>
}
</pre>
</div> <!-- end type PHImageRequestOptionsVersion -->
<div> <!-- start type PHImageResultHandler -->
<h3>New Type Photos.PHImageResultHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHImageResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHImageResultHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (UIKit.UIImage result, Foundation.NSDictionary info, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (UIKit.UIImage result, Foundation.NSDictionary info);</span>
}
</pre>
</div> <!-- end type PHImageResultHandler -->
<div> <!-- start type PHLivePhoto -->
<h3>New Type Photos.PHLivePhoto</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhoto : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhoto ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhoto (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhoto (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhoto (IntPtr handle);</span>
	// fields
	<span class='added added-field ' data-is-non-breaking="">public static const int RequestIdInvalid;</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreGraphics.CGSize Size { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CancelLivePhotoRequest (int requestID);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static int RequestLivePhoto (Foundation.NSUrl[] fileUrls, UIKit.UIImage image, CoreGraphics.CGSize targetSize, PHImageContentMode contentMode, System.Action&lt;PHLivePhoto,Foundation.NSDictionary&gt; resultHandler);</span>
}
</pre>
</div> <!-- end type PHLivePhoto -->
<div> <!-- start type PHLivePhotoEditingContext -->
<h3>New Type Photos.PHLivePhotoEditingContext</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoEditingContext : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoEditingContext (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoEditingContext (PHContentEditingInput livePhotoInput);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoEditingContext (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual float AudioVolume { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime Duration { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHLivePhotoFrameProcessingBlock FrameProcessor { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreImage.CIImage FullSizeImage { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual ImageIO.CGImagePropertyOrientation Orientation { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual CoreMedia.CMTime PhotoTime { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Cancel ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PrepareLivePhotoForPlayback (CoreGraphics.CGSize targetSize, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;PHLivePhoto,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;PHLivePhoto&gt; PrepareLivePhotoForPlaybackAsync (CoreGraphics.CGSize targetSize, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void SaveLivePhoto (PHContentEditingOutput output, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options, System.Action&lt;System.Boolean,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; SaveLivePhotoAsync (PHContentEditingOutput output, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; options);</span>
}
</pre>
</div> <!-- end type PHLivePhotoEditingContext -->
<div> <!-- start type PHLivePhotoFrameProcessingBlock -->
<h3>New Type Photos.PHLivePhotoFrameProcessingBlock</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHLivePhotoFrameProcessingBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoFrameProcessingBlock (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (IPHLivePhotoFrame frame, Foundation.NSError error, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual CoreImage.CIImage Invoke (IPHLivePhotoFrame frame, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type PHLivePhotoFrameProcessingBlock -->
<div> <!-- start type PHLivePhotoFrameType -->
<h3>New Type Photos.PHLivePhotoFrameType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHLivePhotoFrameType {
	<span class='added added-field ' data-is-non-breaking="">Photo = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 1,</span>
}
</pre>
</div> <!-- end type PHLivePhotoFrameType -->
<div> <!-- start type PHLivePhotoInfo -->
<h3>New Type Photos.PHLivePhotoInfo</h3>
<pre class='added' data-is-non-breaking="">
public static class PHLivePhotoInfo {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CancelledKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString ErrorKey { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString IsDegradedKey { get; }</span>
}
</pre>
</div> <!-- end type PHLivePhotoInfo -->
<div> <!-- start type PHLivePhotoRequestOptions -->
<h3>New Type Photos.PHLivePhotoRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoRequestOptions : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHImageRequestOptionsVersion Version { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHLivePhotoRequestOptions -->
<div> <!-- start type PHObject -->
<h3>New Type Photos.PHObject</h3>
<pre class='added' data-is-non-breaking="">
public class PHObject : Foundation.NSObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObject (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalIdentifier { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type PHObject -->
<div> <!-- start type PHObjectChangeDetails -->
<h3>New Type Photos.PHObjectChangeDetails</h3>
<pre class='added' data-is-non-breaking="">
public class PHObjectChangeDetails : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHObjectChangeDetails ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectChangeDetails (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool AssetContentChanged { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectAfterChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject ObjectBeforeChanges { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ObjectWasDeleted { get; }</span>
}
</pre>
</div> <!-- end type PHObjectChangeDetails -->
<div> <!-- start type PHObjectPlaceholder -->
<h3>New Type Photos.PHObjectPlaceholder</h3>
<pre class='added' data-is-non-breaking="">
public class PHObjectPlaceholder : Photos.PHObject, Foundation.INSCopying, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHObjectPlaceholder ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectPlaceholder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHObjectPlaceholder (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type PHObjectPlaceholder -->
<div> <!-- start type PHPhotoLibrary -->
<h3>New Type Photos.PHPhotoLibrary</h3>
<pre class='added' data-is-non-breaking="">
public class PHPhotoLibrary : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibrary (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PHAuthorizationStatus AuthorizationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static PHPhotoLibrary SharedPhotoLibrary { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PerformChanges (System.Action changeHandler, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual bool PerformChangesAndWait (System.Action changeHandler, out Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RegisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public object RegisterChangeObserver (System.Action&lt;PHChange&gt; changeObserver);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void RequestAuthorization (System.Action&lt;PHAuthorizationStatus&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UnregisterChangeObserver (IPHPhotoLibraryChangeObserver observer);</span>
	<span class='added added-method ' data-is-non-breaking="">public void UnregisterChangeObserver (object registeredToken);</span>
}
</pre>
</div> <!-- end type PHPhotoLibrary -->
<div> <!-- start type PHPhotoLibraryChangeObserver -->
<h3>New Type Photos.PHPhotoLibraryChangeObserver</h3>
<pre class='added' data-is-non-breaking="">
public abstract class PHPhotoLibraryChangeObserver : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPHPhotoLibraryChangeObserver, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHPhotoLibraryChangeObserver (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void PhotoLibraryDidChange (PHChange changeInstance);</span>
}
</pre>
</div> <!-- end type PHPhotoLibraryChangeObserver -->
<div> <!-- start type PHProgressHandler -->
<h3>New Type Photos.PHProgressHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate PHProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHProgressHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (double progress, ref bool stop, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (double progress, ref bool stop);</span>
}
</pre>
</div> <!-- end type PHProgressHandler -->
<div> <!-- start type PHVideoRequestOptions -->
<h3>New Type Photos.PHVideoRequestOptions</h3>
<pre class='added' data-is-non-breaking="">
public class PHVideoRequestOptions : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHVideoRequestOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHVideoRequestOptions (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHVideoRequestOptions (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHVideoRequestOptionsDeliveryMode DeliveryMode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool NetworkAccessAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHAssetVideoProgressHandler ProgressHandler { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual PHVideoRequestOptionsVersion Version { get; set; }</span>
}
</pre>
</div> <!-- end type PHVideoRequestOptions -->
<div> <!-- start type PHVideoRequestOptionsDeliveryMode -->
<h3>New Type Photos.PHVideoRequestOptionsDeliveryMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHVideoRequestOptionsDeliveryMode {
	<span class='added added-field ' data-is-non-breaking="">Automatic = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">FastFormat = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">HighQualityFormat = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">MediumQualityFormat = 2,</span>
}
</pre>
</div> <!-- end type PHVideoRequestOptionsDeliveryMode -->
<div> <!-- start type PHVideoRequestOptionsVersion -->
<h3>New Type Photos.PHVideoRequestOptionsVersion</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHVideoRequestOptionsVersion {
	<span class='added added-field ' data-is-non-breaking="">Current = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Original = 1,</span>
}
</pre>
</div> <!-- end type PHVideoRequestOptionsVersion -->
</div> <!-- end namespace Photos -->

<!-- start namespace PhotosUI --> <div> 
<h2>New Namespace PhotosUI</h2>

<div> <!-- start type IPHLivePhotoViewDelegate -->
<h3>New Type PhotosUI.IPHLivePhotoViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IPHLivePhotoViewDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IPHLivePhotoViewDelegate -->
<div> <!-- start type PHLivePhotoBadgeOptions -->
<h3>New Type PhotosUI.PHLivePhotoBadgeOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum PHLivePhotoBadgeOptions {
	<span class='added added-field ' data-is-non-breaking="">LiveOff = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">OverContent = 1,</span>
}
</pre>
</div> <!-- end type PHLivePhotoBadgeOptions -->
<div> <!-- start type PHLivePhotoView -->
<h3>New Type PhotosUI.PHLivePhotoView</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoView : UIKit.UIView, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAccessibilityIdentification, UIKit.IUIAppearance, UIKit.IUIAppearanceContainer, UIKit.IUICoordinateSpace, UIKit.IUIDynamicItem, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoView ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoView (CoreGraphics.CGRect frame);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoView (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoView (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoView (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static PHLivePhotoView.PHLivePhotoViewAppearance Appearance { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public IPHLivePhotoViewDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Photos.PHLivePhoto LivePhoto { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Muted { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UIKit.UIGestureRecognizer PlaybackGestureRecognizer { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSObject WeakDelegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static PHLivePhotoView.PHLivePhotoViewAppearance AppearanceWhenContainedIn (System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance&lt;T&gt; ();</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance (UIKit.UITraitCollection traits);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance&lt;T&gt; (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static PHLivePhotoView.PHLivePhotoViewAppearance GetAppearance (UIKit.UITraitCollection traits, System.Type[] containers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UIKit.UIImage GetLivePhotoBadgeImage (PHLivePhotoBadgeOptions badgeOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartPlayback (PHLivePhotoViewPlaybackStyle playbackStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopPlayback ();</span>

	// inner types
	public class PHLivePhotoViewAppearance : UIKit.UIView+UIViewAppearance, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearance {
		// constructors
		<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoView (IntPtr handle);</span>
	}
}
</pre>
</div> <!-- end type PHLivePhotoView -->
<div> <!-- start type PHLivePhotoViewDelegate -->
<h3>New Type PhotosUI.PHLivePhotoViewDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class PHLivePhotoViewDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IPHLivePhotoViewDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public PHLivePhotoViewDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoViewDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected PHLivePhotoViewDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidEndPlayback (PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillBeginPlayback (PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);</span>
}
</pre>
</div> <!-- end type PHLivePhotoViewDelegate -->
<div> <!-- start type PHLivePhotoViewDelegate_Extensions -->
<h3>New Type PhotosUI.PHLivePhotoViewDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class PHLivePhotoViewDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidEndPlayback (IPHLivePhotoViewDelegate This, PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void WillBeginPlayback (IPHLivePhotoViewDelegate This, PHLivePhotoView livePhotoView, PHLivePhotoViewPlaybackStyle playbackStyle);</span>
}
</pre>
</div> <!-- end type PHLivePhotoViewDelegate_Extensions -->
<div> <!-- start type PHLivePhotoViewPlaybackStyle -->
<h3>New Type PhotosUI.PHLivePhotoViewPlaybackStyle</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum PHLivePhotoViewPlaybackStyle {
	<span class='added added-field ' data-is-non-breaking="">Full = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Hint = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Undefined = 0,</span>
}
</pre>
</div> <!-- end type PHLivePhotoViewPlaybackStyle -->
</div> <!-- end namespace PhotosUI -->

<!-- start namespace ReplayKit --> <div> 
<h2>New Namespace ReplayKit</h2>

<div> <!-- start type IRPBroadcastActivityViewControllerDelegate -->
<h3>New Type ReplayKit.IRPBroadcastActivityViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IRPBroadcastActivityViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (RPBroadcastActivityViewController broadcastActivityViewController, RPBroadcastController broadcastController, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type IRPBroadcastActivityViewControllerDelegate -->
<div> <!-- start type IRPBroadcastControllerDelegate -->
<h3>New Type ReplayKit.IRPBroadcastControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IRPBroadcastControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IRPBroadcastControllerDelegate -->
<div> <!-- start type IRPPreviewViewControllerDelegate -->
<h3>New Type ReplayKit.IRPPreviewViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IRPPreviewViewControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IRPPreviewViewControllerDelegate -->
<div> <!-- start type IRPScreenRecorderDelegate -->
<h3>New Type ReplayKit.IRPScreenRecorderDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IRPScreenRecorderDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IRPScreenRecorderDelegate -->
<div> <!-- start type LoadBroadcastingHandler -->
<h3>New Type ReplayKit.LoadBroadcastingHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate LoadBroadcastingHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public LoadBroadcastingHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (string bundleID, string displayName, UIKit.UIImage appIcon, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (string bundleID, string displayName, UIKit.UIImage appIcon);</span>
}
</pre>
</div> <!-- end type LoadBroadcastingHandler -->
<div> <!-- start type NSExtensionContext_RPBroadcastExtension -->
<h3>New Type ReplayKit.NSExtensionContext_RPBroadcastExtension</h3>
<pre class='added' data-is-non-breaking="">
public static class NSExtensionContext_RPBroadcastExtension {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void CompleteRequest (Foundation.NSExtensionContext This, Foundation.NSUrl broadcastURL, RPBroadcastConfiguration broadcastConfiguration, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSCoding&gt; setupInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadBroadcastingApplicationInfo (Foundation.NSExtensionContext This, LoadBroadcastingHandler handler);</span>
}
</pre>
</div> <!-- end type NSExtensionContext_RPBroadcastExtension -->
<div> <!-- start type RPBroadcastActivityViewController -->
<h3>New Type ReplayKit.RPBroadcastActivityViewController</h3>
<pre class='added' data-is-non-breaking="">
public class RPBroadcastActivityViewController : UIKit.UIViewController, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastActivityViewController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastActivityViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastActivityViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastActivityViewController (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastActivityViewController (string nibName, Foundation.NSBundle bundle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IRPBroadcastActivityViewControllerDelegate Delegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void LoadBroadcastActivityViewController (System.Action&lt;RPBroadcastActivityViewController,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;RPBroadcastActivityViewController&gt; LoadBroadcastActivityViewControllerAsync ();</span>
}
</pre>
</div> <!-- end type RPBroadcastActivityViewController -->
<div> <!-- start type RPBroadcastActivityViewControllerDelegate -->
<h3>New Type ReplayKit.RPBroadcastActivityViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class RPBroadcastActivityViewControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IRPBroadcastActivityViewControllerDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastActivityViewControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastActivityViewControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastActivityViewControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (RPBroadcastActivityViewController broadcastActivityViewController, RPBroadcastController broadcastController, Foundation.NSError error);</span>
}
</pre>
</div> <!-- end type RPBroadcastActivityViewControllerDelegate -->
<div> <!-- start type RPBroadcastConfiguration -->
<h3>New Type ReplayKit.RPBroadcastConfiguration</h3>
<pre class='added' data-is-non-breaking="">
public class RPBroadcastConfiguration : Foundation.NSObject, Foundation.INSCoding, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastConfiguration ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastConfiguration (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastConfiguration (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastConfiguration (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double ClipDuration { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSNumber,Foundation.INSSecureCoding&gt; VideoCompressionProperties { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type RPBroadcastConfiguration -->
<div> <!-- start type RPBroadcastController -->
<h3>New Type ReplayKit.RPBroadcastController</h3>
<pre class='added' data-is-non-breaking="">
public class RPBroadcastController : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastController (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string BroadcastExtensionBundleID { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSUrl BroadcastUrl { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Broadcasting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IRPBroadcastControllerDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Paused { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,Foundation.INSCoding&gt; ServiceInfo { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishBroadcast (System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task FinishBroadcastAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PauseBroadcast ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ResumeBroadcast ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartBroadcast (System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StartBroadcastAsync ();</span>
}
</pre>
</div> <!-- end type RPBroadcastController -->
<div> <!-- start type RPBroadcastControllerDelegate -->
<h3>New Type ReplayKit.RPBroadcastControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class RPBroadcastControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IRPBroadcastControllerDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (RPBroadcastController broadcastController, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidUpdateServiceInfo (RPBroadcastController broadcastController, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSCoding&gt; serviceInfo);</span>
}
</pre>
</div> <!-- end type RPBroadcastControllerDelegate -->
<div> <!-- start type RPBroadcastControllerDelegate_Extensions -->
<h3>New Type ReplayKit.RPBroadcastControllerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class RPBroadcastControllerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidFinish (IRPBroadcastControllerDelegate This, RPBroadcastController broadcastController, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidUpdateServiceInfo (IRPBroadcastControllerDelegate This, RPBroadcastController broadcastController, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSCoding&gt; serviceInfo);</span>
}
</pre>
</div> <!-- end type RPBroadcastControllerDelegate_Extensions -->
<div> <!-- start type RPBroadcastHandler -->
<h3>New Type ReplayKit.RPBroadcastHandler</h3>
<pre class='added' data-is-non-breaking="">
public class RPBroadcastHandler : Foundation.NSObject, Foundation.INSExtensionRequestHandling, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BeginRequestWithExtensionContext (Foundation.NSExtensionContext context);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void UpdateServiceInfo (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.INSCoding&gt; serviceInfo);</span>
}
</pre>
</div> <!-- end type RPBroadcastHandler -->
<div> <!-- start type RPBroadcastMP4ClipHandler -->
<h3>New Type ReplayKit.RPBroadcastMP4ClipHandler</h3>
<pre class='added' data-is-non-breaking="">
public class RPBroadcastMP4ClipHandler : ReplayKit.RPBroadcastHandler, Foundation.INSExtensionRequestHandling, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastMP4ClipHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastMP4ClipHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastMP4ClipHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void FinishedProcessingMP4Clip (RPBroadcastConfiguration broadcastConfiguration, Foundation.NSError error);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ProcessMP4Clip (Foundation.NSUrl mp4ClipURL, Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; setupInfo, bool finished);</span>
}
</pre>
</div> <!-- end type RPBroadcastMP4ClipHandler -->
<div> <!-- start type RPBroadcastSampleHandler -->
<h3>New Type ReplayKit.RPBroadcastSampleHandler</h3>
<pre class='added' data-is-non-breaking="">
public class RPBroadcastSampleHandler : ReplayKit.RPBroadcastHandler, Foundation.INSExtensionRequestHandling, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPBroadcastSampleHandler ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastSampleHandler (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPBroadcastSampleHandler (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void BroadcastFinished ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BroadcastPaused ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BroadcastResumed ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void BroadcastStarted (Foundation.NSDictionary&lt;Foundation.NSString,Foundation.NSObject&gt; setupInfo);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void ProcessSampleBuffer (CoreMedia.CMSampleBuffer sampleBuffer, RPSampleBufferType sampleBufferType);</span>
}
</pre>
</div> <!-- end type RPBroadcastSampleHandler -->
<div> <!-- start type RPPreviewViewController -->
<h3>New Type ReplayKit.RPPreviewViewController</h3>
<pre class='added' data-is-non-breaking="">
public class RPPreviewViewController : UIKit.UIViewController, Foundation.INSCoding, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.Collections.IEnumerable, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, UIKit.IUIAppearanceContainer, UIKit.IUIContentContainer, UIKit.IUIFocusEnvironment, UIKit.IUITraitEnvironment {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPPreviewViewController ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RPPreviewViewController (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPPreviewViewController (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPPreviewViewController (IntPtr handle);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public RPPreviewViewController (string nibName, Foundation.NSBundle bundle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual RPPreviewViewControllerMode Mode { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IRPPreviewViewControllerDelegate PreviewControllerDelegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
}
</pre>
</div> <!-- end type RPPreviewViewController -->
<div> <!-- start type RPPreviewViewControllerDelegate -->
<h3>New Type ReplayKit.RPPreviewViewControllerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class RPPreviewViewControllerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IRPPreviewViewControllerDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPPreviewViewControllerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPPreviewViewControllerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPPreviewViewControllerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidFinish (RPPreviewViewController previewController);</span>
}
</pre>
</div> <!-- end type RPPreviewViewControllerDelegate -->
<div> <!-- start type RPPreviewViewControllerDelegate_Extensions -->
<h3>New Type ReplayKit.RPPreviewViewControllerDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class RPPreviewViewControllerDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidFinish (IRPPreviewViewControllerDelegate This, RPPreviewViewController previewController);</span>
}
</pre>
</div> <!-- end type RPPreviewViewControllerDelegate_Extensions -->
<div> <!-- start type RPPreviewViewControllerMode -->
<h3>New Type ReplayKit.RPPreviewViewControllerMode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RPPreviewViewControllerMode {
	<span class='added added-field ' data-is-non-breaking="">Preview = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Share = 1,</span>
}
</pre>
</div> <!-- end type RPPreviewViewControllerMode -->
<div> <!-- start type RPRecordingError -->
<h3>New Type ReplayKit.RPRecordingError</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RPRecordingError {
	<span class='added added-field ' data-is-non-breaking="">BroadcastInvalidSession = -5808,</span>
	<span class='added added-field ' data-is-non-breaking="">ContentResize = -5807,</span>
	<span class='added added-field ' data-is-non-breaking="">Disabled = -5802,</span>
	<span class='added added-field ' data-is-non-breaking="">Failed = -5804,</span>
	<span class='added added-field ' data-is-non-breaking="">FailedToStart = -5803,</span>
	<span class='added added-field ' data-is-non-breaking="">InsufficientStorage = -5805,</span>
	<span class='added added-field ' data-is-non-breaking="">Interrupted = -5806,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">SystemDormancy = -5809,</span>
	<span class='added added-field ' data-is-non-breaking="">Unknown = -5800,</span>
	<span class='added added-field ' data-is-non-breaking="">UserDeclined = -5801,</span>
}
</pre>
</div> <!-- end type RPRecordingError -->
<div> <!-- start type RPRecordingErrorExtensions -->
<h3>New Type ReplayKit.RPRecordingErrorExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class RPRecordingErrorExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (RPRecordingError self);</span>
}
</pre>
</div> <!-- end type RPRecordingErrorExtensions -->
<div> <!-- start type RPSampleBufferType -->
<h3>New Type ReplayKit.RPSampleBufferType</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum RPSampleBufferType {
	<span class='added added-field ' data-is-non-breaking="">AudioApp = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">AudioMic = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">Video = 1,</span>
}
</pre>
</div> <!-- end type RPSampleBufferType -->
<div> <!-- start type RPScreenRecorder -->
<h3>New Type ReplayKit.RPScreenRecorder</h3>
<pre class='added' data-is-non-breaking="">
public class RPScreenRecorder : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected RPScreenRecorder (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPScreenRecorder (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Available { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IRPScreenRecorderDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Recording { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static RPScreenRecorder SharedRecorder { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DiscardRecording (System.Action handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task DiscardRecordingAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartRecording (System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StartRecording (bool microphoneEnabled, System.Action&lt;Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StartRecordingAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task StartRecordingAsync (bool microphoneEnabled);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void StopRecording (System.Action&lt;RPPreviewViewController,Foundation.NSError&gt; handler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;RPPreviewViewController&gt; StopRecordingAsync ();</span>
}
</pre>
</div> <!-- end type RPScreenRecorder -->
<div> <!-- start type RPScreenRecorderDelegate -->
<h3>New Type ReplayKit.RPScreenRecorderDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class RPScreenRecorderDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, IRPScreenRecorderDelegate, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public RPScreenRecorderDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPScreenRecorderDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected RPScreenRecorderDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidChangeAvailability (RPScreenRecorder screenRecorder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void DidStopRecording (RPScreenRecorder screenRecorder, Foundation.NSError error, RPPreviewViewController previewViewController);</span>
}
</pre>
</div> <!-- end type RPScreenRecorderDelegate -->
<div> <!-- start type RPScreenRecorderDelegate_Extensions -->
<h3>New Type ReplayKit.RPScreenRecorderDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class RPScreenRecorderDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void DidChangeAvailability (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void DidStopRecording (IRPScreenRecorderDelegate This, RPScreenRecorder screenRecorder, Foundation.NSError error, RPPreviewViewController previewViewController);</span>
}
</pre>
</div> <!-- end type RPScreenRecorderDelegate_Extensions -->
</div> <!-- end namespace ReplayKit -->

<!-- start namespace UserNotifications --> <div> 
<h2>New Namespace UserNotifications</h2>

<div> <!-- start type IUNUserNotificationCenterDelegate -->
<h3>New Type UserNotifications.IUNUserNotificationCenterDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IUNUserNotificationCenterDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
</div> <!-- end type IUNUserNotificationCenterDelegate -->
<div> <!-- start type UNAuthorizationOptions -->
<h3>New Type UserNotifications.UNAuthorizationOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum UNAuthorizationOptions {
	<span class='added added-field ' data-is-non-breaking="">Alert = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Badge = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">CarPlay = 8,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Sound = 2,</span>
}
</pre>
</div> <!-- end type UNAuthorizationOptions -->
<div> <!-- start type UNAuthorizationStatus -->
<h3>New Type UserNotifications.UNAuthorizationStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UNAuthorizationStatus {
	<span class='added added-field ' data-is-non-breaking="">Authorized = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Denied = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
}
</pre>
</div> <!-- end type UNAuthorizationStatus -->
<div> <!-- start type UNCalendarNotificationTrigger -->
<h3>New Type UserNotifications.UNCalendarNotificationTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class UNCalendarNotificationTrigger : UserNotifications.UNNotificationTrigger, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNCalendarNotificationTrigger (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNCalendarNotificationTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNCalendarNotificationTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDateComponents DateComponents { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate NextTriggerDate { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UNCalendarNotificationTrigger Trigger (Foundation.NSDateComponents dateComponents, bool repeats);</span>
}
</pre>
</div> <!-- end type UNCalendarNotificationTrigger -->
<div> <!-- start type UNErrorCode -->
<h3>New Type UserNotifications.UNErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UNErrorCode {
	<span class='added added-field ' data-is-non-breaking="">AttachmentCorrupt = 105,</span>
	<span class='added added-field ' data-is-non-breaking="">AttachmentInvalidFileSize = 102,</span>
	<span class='added added-field ' data-is-non-breaking="">AttachmentInvalidUrl = 100,</span>
	<span class='added added-field ' data-is-non-breaking="">AttachmentMoveIntoDataStoreFailed = 104,</span>
	<span class='added added-field ' data-is-non-breaking="">AttachmentNotInDataStore = 103,</span>
	<span class='added added-field ' data-is-non-breaking="">AttachmentUnrecognizedType = 101,</span>
	<span class='added added-field ' data-is-non-breaking="">NotificationInvalidNoContent = 1401,</span>
	<span class='added added-field ' data-is-non-breaking="">NotificationInvalidNoDate = 1400,</span>
	<span class='added added-field ' data-is-non-breaking="">NotificationsNotAllowed = 1,</span>
}
</pre>
</div> <!-- end type UNErrorCode -->
<div> <!-- start type UNErrorCodeExtensions -->
<h3>New Type UserNotifications.UNErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UNErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (UNErrorCode self);</span>
}
</pre>
</div> <!-- end type UNErrorCodeExtensions -->
<div> <!-- start type UNMutableNotificationContent -->
<h3>New Type UserNotifications.UNMutableNotificationContent</h3>
<pre class='added' data-is-non-breaking="">
public class UNMutableNotificationContent : UserNotifications.UNNotificationContent, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNMutableNotificationContent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UNMutableNotificationContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNMutableNotificationContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNMutableNotificationContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Badge { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDictionary UserInfo { get; set; }</span>
}
</pre>
</div> <!-- end type UNMutableNotificationContent -->
<div> <!-- start type UNNotification -->
<h3>New Type UserNotifications.UNNotification</h3>
<pre class='added' data-is-non-breaking="">
public class UNNotification : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNNotification (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotification (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotification (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate Date { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UNNotificationRequest Request { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type UNNotification -->
<div> <!-- start type UNNotificationContent -->
<h3>New Type UserNotifications.UNNotificationContent</h3>
<pre class='added' data-is-non-breaking="">
public class UNNotificationContent : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNNotificationContent ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public UNNotificationContent (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationContent (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationContent (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSNumber Badge { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);</span>
}
</pre>
</div> <!-- end type UNNotificationContent -->
<div> <!-- start type UNNotificationPresentationOptions -->
<h3>New Type UserNotifications.UNNotificationPresentationOptions</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
[Flags]
public enum UNNotificationPresentationOptions {
	<span class='added added-field ' data-is-non-breaking="">Alert = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">Badge = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Sound = 2,</span>
}
</pre>
</div> <!-- end type UNNotificationPresentationOptions -->
<div> <!-- start type UNNotificationRequest -->
<h3>New Type UserNotifications.UNNotificationRequest</h3>
<pre class='added' data-is-non-breaking="">
public class UNNotificationRequest : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNNotificationRequest (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UNNotificationContent Content { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string Identifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UNNotificationTrigger Trigger { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
	<span class='added added-method ' data-is-non-breaking="">public static UNNotificationRequest FromIdentifier (string identifier, UNNotificationContent content, UNNotificationTrigger trigger);</span>
}
</pre>
</div> <!-- end type UNNotificationRequest -->
<div> <!-- start type UNNotificationSetting -->
<h3>New Type UserNotifications.UNNotificationSetting</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum UNNotificationSetting {
	<span class='added added-field ' data-is-non-breaking="">Disabled = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">Enabled = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">NotSupported = 0,</span>
}
</pre>
</div> <!-- end type UNNotificationSetting -->
<div> <!-- start type UNNotificationSettings -->
<h3>New Type UserNotifications.UNNotificationSettings</h3>
<pre class='added' data-is-non-breaking="">
public class UNNotificationSettings : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNNotificationSettings (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationSettings (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationSettings (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual UNAuthorizationStatus AuthorizationStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual UNNotificationSetting BadgeSetting { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type UNNotificationSettings -->
<div> <!-- start type UNNotificationTrigger -->
<h3>New Type UserNotifications.UNNotificationTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class UNNotificationTrigger : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNNotificationTrigger (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNNotificationTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool Repeats { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual Foundation.NSObject Copy (Foundation.NSZone zone);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EncodeTo (Foundation.NSCoder encoder);</span>
}
</pre>
</div> <!-- end type UNNotificationTrigger -->
<div> <!-- start type UNPushNotificationTrigger -->
<h3>New Type UserNotifications.UNPushNotificationTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class UNPushNotificationTrigger : UserNotifications.UNNotificationTrigger, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNPushNotificationTrigger (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNPushNotificationTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNPushNotificationTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
}
</pre>
</div> <!-- end type UNPushNotificationTrigger -->
<div> <!-- start type UNTimeIntervalNotificationTrigger -->
<h3>New Type UserNotifications.UNTimeIntervalNotificationTrigger</h3>
<pre class='added' data-is-non-breaking="">
public class UNTimeIntervalNotificationTrigger : UserNotifications.UNNotificationTrigger, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSObjectProtocol, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNTimeIntervalNotificationTrigger (Foundation.NSCoder coder);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNTimeIntervalNotificationTrigger (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNTimeIntervalNotificationTrigger (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate NextTriggerDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual double TimeInterval { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static UNTimeIntervalNotificationTrigger Trigger (double timeInterval, bool repeats);</span>
}
</pre>
</div> <!-- end type UNTimeIntervalNotificationTrigger -->
<div> <!-- start type UNUserNotificationCenter -->
<h3>New Type UserNotifications.UNUserNotificationCenter</h3>
<pre class='added' data-is-non-breaking="">
public class UNUserNotificationCenter : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected UNUserNotificationCenter (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNUserNotificationCenter (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static UNUserNotificationCenter CurrentNotificationCenter { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IUNUserNotificationCenterDelegate Delegate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool SupportsContentExtensions { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void AddNotificationRequest (UNNotificationRequest request, System.Action&lt;Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task AddNotificationRequestAsync (UNNotificationRequest request);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetNotificationSettings (System.Action&lt;UNNotificationSettings&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;UNNotificationSettings&gt; GetNotificationSettingsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetPendingNotificationRequests (System.Action&lt;UNNotificationRequest[]&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;UNNotificationRequest[]&gt; GetPendingNotificationRequestsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemoveAllPendingNotificationRequests ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RemovePendingNotificationRequests (string[] identifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void RequestAuthorization (UNAuthorizationOptions options, System.Action&lt;System.Boolean,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;System.Tuple&lt;System.Boolean,Foundation.NSError&gt;&gt; RequestAuthorizationAsync (UNAuthorizationOptions options);</span>
}
</pre>
</div> <!-- end type UNUserNotificationCenter -->
<div> <!-- start type UNUserNotificationCenterDelegate -->
<h3>New Type UserNotifications.UNUserNotificationCenterDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class UNUserNotificationCenterDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IUNUserNotificationCenterDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public UNUserNotificationCenterDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNUserNotificationCenterDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected UNUserNotificationCenterDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void WillPresentNotification (UNUserNotificationCenter center, UNNotification notification, System.Action&lt;UNNotificationPresentationOptions&gt; completionHandler);</span>
}
</pre>
</div> <!-- end type UNUserNotificationCenterDelegate -->
<div> <!-- start type UNUserNotificationCenterDelegate_Extensions -->
<h3>New Type UserNotifications.UNUserNotificationCenterDelegate_Extensions</h3>
<pre class='added' data-is-non-breaking="">
public static class UNUserNotificationCenterDelegate_Extensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static void WillPresentNotification (IUNUserNotificationCenterDelegate This, UNUserNotificationCenter center, UNNotification notification, System.Action&lt;UNNotificationPresentationOptions&gt; completionHandler);</span>
}
</pre>
</div> <!-- end type UNUserNotificationCenterDelegate_Extensions -->
</div> <!-- end namespace UserNotifications -->

<!-- start namespace VideoSubscriberAccount --> <div> 
<h2>New Namespace VideoSubscriberAccount</h2>

<div> <!-- start type IVSAccountManagerDelegate -->
<h3>New Type VideoSubscriberAccount.IVSAccountManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public interface IVSAccountManagerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DismissViewController (VSAccountManager accountManager, UIKit.UIViewController viewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PresentViewController (VSAccountManager accountManager, UIKit.UIViewController viewController);</span>
}
</pre>
</div> <!-- end type IVSAccountManagerDelegate -->
<div> <!-- start type VSAccountAccessStatus -->
<h3>New Type VideoSubscriberAccount.VSAccountAccessStatus</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VSAccountAccessStatus {
	<span class='added added-field ' data-is-non-breaking="">Denied = 2,</span>
	<span class='added added-field ' data-is-non-breaking="">Granted = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">NotDetermined = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">Restricted = 1,</span>
}
</pre>
</div> <!-- end type VSAccountAccessStatus -->
<div> <!-- start type VSAccountManager -->
<h3>New Type VideoSubscriberAccount.VSAccountManager</h3>
<pre class='added' data-is-non-breaking="">
public class VSAccountManager : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VSAccountManager ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountManager (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountManager (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual IVSAccountManagerDelegate Delegate { get; set; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void CheckAccessStatus (Foundation.NSDictionary options, System.Action&lt;VSAccountAccessStatus,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void CheckAccessStatus (VSAccountManagerAccessOptions accessOptions, System.Action&lt;VSAccountAccessStatus,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;VSAccountAccessStatus&gt; CheckAccessStatusAsync (Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;VSAccountAccessStatus&gt; CheckAccessStatusAsync (VSAccountManagerAccessOptions accessOptions);</span>
	<span class='added added-method ' data-is-non-breaking="">protected override void Dispose (bool disposing);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual VSAccountManagerResult EnqueueAccountMetadataRequest (VSAccountMetadataRequest request, System.Action&lt;VSAccountMetadata,Foundation.NSError&gt; completionHandler);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;VSAccountMetadata&gt; EnqueueAccountMetadataRequestAsync (VSAccountMetadataRequest request);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;VSAccountMetadata&gt; EnqueueAccountMetadataRequestAsync (VSAccountMetadataRequest request, out VSAccountManagerResult result);</span>
}
</pre>
</div> <!-- end type VSAccountManager -->
<div> <!-- start type VSAccountManagerAccessOptions -->
<h3>New Type VideoSubscriberAccount.VSAccountManagerAccessOptions</h3>
<pre class='added' data-is-non-breaking="">
public class VSAccountManagerAccessOptions : Foundation.DictionaryContainer {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VSAccountManagerAccessOptions ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">public VSAccountManagerAccessOptions (Foundation.NSDictionary dictionary);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public bool? CheckAccessOptionPrompt { get; set; }</span>
}
</pre>
</div> <!-- end type VSAccountManagerAccessOptions -->
<div> <!-- start type VSAccountManagerDelegate -->
<h3>New Type VideoSubscriberAccount.VSAccountManagerDelegate</h3>
<pre class='added' data-is-non-breaking="">
public abstract class VSAccountManagerDelegate : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt;, IVSAccountManagerDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountManagerDelegate ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountManagerDelegate (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountManagerDelegate (IntPtr handle);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void DismissViewController (VSAccountManager accountManager, UIKit.UIViewController viewController);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void PresentViewController (VSAccountManager accountManager, UIKit.UIViewController viewController);</span>
}
</pre>
</div> <!-- end type VSAccountManagerDelegate -->
<div> <!-- start type VSAccountManagerResult -->
<h3>New Type VideoSubscriberAccount.VSAccountManagerResult</h3>
<pre class='added' data-is-non-breaking="">
public class VSAccountManagerResult : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountManagerResult (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountManagerResult (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual void Cancel ();</span>
}
</pre>
</div> <!-- end type VSAccountManagerResult -->
<div> <!-- start type VSAccountMetadata -->
<h3>New Type VideoSubscriberAccount.VSAccountMetadata</h3>
<pre class='added' data-is-non-breaking="">
public class VSAccountMetadata : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VSAccountMetadata ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountMetadata (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountMetadata (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string AccountProviderIdentifier { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSDate AuthenticationExpirationDate { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string SamlAttributeQueryResponse { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual Foundation.NSData VerificationData { get; }</span>
}
</pre>
</div> <!-- end type VSAccountMetadata -->
<div> <!-- start type VSAccountMetadataRequest -->
<h3>New Type VideoSubscriberAccount.VSAccountMetadataRequest</h3>
<pre class='added' data-is-non-breaking="">
public class VSAccountMetadataRequest : Foundation.NSObject, Foundation.INSObjectProtocol, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public VSAccountMetadataRequest ();</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountMetadataRequest (Foundation.NSObjectFlag t);</span>
	<span class='added added-constructor ' data-is-non-breaking="">protected VSAccountMetadataRequest (IntPtr handle);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] AttributeNames { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string ChannelIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public override IntPtr ClassHandle { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool ForceAuthentication { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeAccountProviderIdentifier { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool IncludeAuthenticationExpirationDate { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual bool InterruptionAllowed { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string LocalizedVideoTitle { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string[] SupportedAccountProviderIdentifiers { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public virtual string VerificationToken { get; set; }</span>
}
</pre>
</div> <!-- end type VSAccountMetadataRequest -->
<div> <!-- start type VSCheckAccessOptionKeys -->
<h3>New Type VideoSubscriberAccount.VSCheckAccessOptionKeys</h3>
<pre class='added' data-is-non-breaking="">
public static class VSCheckAccessOptionKeys {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString CheckAccessOptionPrompt { get; }</span>
}
</pre>
</div> <!-- end type VSCheckAccessOptionKeys -->
<div> <!-- start type VSErrorCode -->
<h3>New Type VideoSubscriberAccount.VSErrorCode</h3>
<pre class='added' data-is-non-breaking="">
[Serializable]
public enum VSErrorCode {
	<span class='added added-field ' data-is-non-breaking="">AccessNotGranted = 0,</span>
	<span class='added added-field ' data-is-non-breaking="">InvalidVerificationToken = 5,</span>
	<span class='added added-field ' data-is-non-breaking="">ProviderRejected = 4,</span>
	<span class='added added-field ' data-is-non-breaking="">ServiceTemporarilyUnavailable = 3,</span>
	<span class='added added-field ' data-is-non-breaking="">UnsupportedProvider = 1,</span>
	<span class='added added-field ' data-is-non-breaking="">UserCancelled = 2,</span>
}
</pre>
</div> <!-- end type VSErrorCode -->
<div> <!-- start type VSErrorCodeExtensions -->
<h3>New Type VideoSubscriberAccount.VSErrorCodeExtensions</h3>
<pre class='added' data-is-non-breaking="">
public static class VSErrorCodeExtensions {
	// methods
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSString GetDomain (VSErrorCode self);</span>
}
</pre>
</div> <!-- end type VSErrorCodeExtensions -->
<div> <!-- start type VSErrorInfoKey -->
<h3>New Type VideoSubscriberAccount.VSErrorInfoKey</h3>
<pre class='added' data-is-non-breaking="">
public static class VSErrorInfoKey {
	// properties
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SamlResponse { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString SamlResponseStatus { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static Foundation.NSString UnsupportedProviderIdentifier { get; }</span>
}
</pre>
</div> <!-- end type VSErrorInfoKey -->
</div> <!-- end namespace VideoSubscriberAccount -->

</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/MonoTouch.NUnitLite.html'>MonoTouch.NUnitLite.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace MonoTouch.NUnit.UI --> <div> 
<h2>Namespace MonoTouch.NUnit.UI</h2>
<!-- start type TouchOptions --> <div>
<h3>Type Changed: MonoTouch.NUnit.UI.TouchOptions</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public string Transport { get; set; }</span>
</pre>
</div>

</div> <!-- end type TouchOptions -->

</div> <!-- end namespace MonoTouch.NUnit.UI -->
<!-- start namespace NUnit.Framework --> <div> 
<h2>Namespace NUnit.Framework</h2>
<!-- start type Assert --> <div>
<h3>Type Changed: NUnit.Framework.Assert</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (object anObject, string message, object[] args);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual, string message);</span>
	<span class='added added-method ' data-is-non-breaking="">public static void IsInstanceOfType (System.Type expected, object actual, string message, object[] args);</span>
</pre>
</div>

</div> <!-- end type Assert -->

</div> <!-- end namespace NUnit.Framework -->
<!-- start namespace NUnit.Framework.Internal --> <div> 
<h2>Namespace NUnit.Framework.Internal</h2>
<!-- start type NUnitLiteTestAssemblyRunner --> <div>
<h3>Type Changed: NUnit.Framework.Internal.NUnitLiteTestAssemblyRunner</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public NUnitLiteTestAssemblyRunner (NUnit.Framework.Api.ITestAssemblyBuilder builder);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public NUnitLiteTestAssemblyRunner (NUnit.Framework.Api.ITestAssemblyBuilder builder, FinallyDelegate finallyDelegate);</span>
</pre>
</div>

</div> <!-- end type NUnitLiteTestAssemblyRunner -->
<!-- start type Test --> <div>
<h3>Type Changed: NUnit.Framework.Internal.Test</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate finD);</span>
</pre>
</div>

</div> <!-- end type Test -->
<!-- start type TestMethod --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestMethod</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type TestMethod -->
<!-- start type TestResult --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestResult</h3>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">public bool ThreadCrashFail;</span>
</pre>
</div>

</div> <!-- end type TestResult -->
<!-- start type TestSuite --> <div>
<h3>Type Changed: NUnit.Framework.Internal.TestSuite</h3>
<p>Removed method:</p>

<pre>
	<span class='removed removed-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter, FinallyDelegate finD);</span>
</pre>
</div>

</div> <!-- end type TestSuite -->
<div> <!-- start type FinallyDelegate -->
<h3>New Type NUnit.Framework.Internal.FinallyDelegate</h3>
<pre class='added' data-is-non-breaking="">
public class FinallyDelegate {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public FinallyDelegate ();</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public void Complete ();</span>
	<span class='added added-method ' data-is-non-breaking="">public void HandleUnhandledExc (System.Exception ex);</span>
	<span class='added added-method ' data-is-non-breaking="">public void Set (TestExecutionContext context, long startTicks, TestResult result);</span>
}
</pre>
</div> <!-- end type FinallyDelegate -->

</div> <!-- end namespace NUnit.Framework.Internal -->
<!-- start namespace NUnit.Framework.Internal.WorkItems --> <div> 
<h2>Namespace NUnit.Framework.Internal.WorkItems</h2>
<!-- start type CompositeWorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.CompositeWorkItem</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Api.ITestFilter childFilter);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Api.ITestFilter childFilter, NUnit.Framework.Internal.FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type CompositeWorkItem -->
<!-- start type SimpleWorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.SimpleWorkItem</h3>
<p>Removed constructors:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command);</span>
	<span class='removed removed-constructor breaking' data-is-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test);</span>
</pre>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command, NUnit.Framework.Internal.FinallyDelegate fd);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test, NUnit.Framework.Internal.FinallyDelegate fd);</span>
</pre>
</div>

</div> <!-- end type SimpleWorkItem -->
<!-- start type WorkItem --> <div>
<h3>Type Changed: NUnit.Framework.Internal.WorkItems.WorkItem</h3>
<p>Removed constructor:</p>

<pre>
	<span class='removed removed-constructor breaking' data-is-breaking="">public WorkItem (NUnit.Framework.Internal.Test test);</span>
</pre>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public WorkItem (NUnit.Framework.Internal.Test test, NUnit.Framework.Internal.FinallyDelegate finallyDelegate);</span>
</pre>
</div>
<div>
<p>Added field:</p>
<pre>
	<span class='added added-field ' data-is-non-breaking="">protected NUnit.Framework.Internal.FinallyDelegate finD;</span>
</pre>
</div>

</div> <!-- end type WorkItem -->

</div> <!-- end namespace NUnit.Framework.Internal.WorkItems -->
<!-- start namespace NUnitLite.Runner --> <div> 
<h2>Namespace NUnitLite.Runner</h2>
<!-- start type TextUI --> <div>
<h3>Type Changed: NUnitLite.Runner.TextUI</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public void TopLevelHandler (object sender, System.UnhandledExceptionEventArgs e);</span>
</pre>
</div>

</div> <!-- end type TextUI -->

</div> <!-- end namespace NUnitLite.Runner -->
</div>



   


 <hr>

 <style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script><h1 id='diff/xi/Xamarin.TVOS/System.Net.Http.html'>System.Net.Http.dll</h1>

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace System.Net.Http --> <div> 
<h2>Namespace System.Net.Http</h2>
<!-- start type HttpClientHandler --> <div>
<h3>Type Changed: System.Net.Http.HttpClientHandler</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public bool CheckCertificateRevocationList { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Cryptography.X509Certificates.X509CertificateCollection ClientCertificates { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Net.ICredentials DefaultProxyCredentials { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxConnectionsPerServer { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public int MaxResponseHeadersLength { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Collections.Generic.IDictionary&lt;System.String,System.Object&gt; Properties { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Func&lt;HttpRequestMessage,System.Security.Cryptography.X509Certificates.X509Certificate2,System.Security.Cryptography.X509Certificates.X509Chain,System.Net.Security.SslPolicyErrors,System.Boolean&gt; ServerCertificateCustomValidationCallback { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public System.Security.Authentication.SslProtocols SslProtocols { get; set; }</span>
</pre>
</div>

</div> <!-- end type HttpClientHandler -->

</div> <!-- end namespace System.Net.Http -->
</div>



   


 <hr>
