---
id: E12ABE8E-BD04-407F-8108-EABE908F35C7
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.App

### Type Changed: Android.App.ActivityManager

Added method:

```
public void MoveTaskToFront (int taskId, int flags);
```

## Namespace Android.App.Admin

### New Type Android.App.Admin.DevicePolicyManagerFlags

```
[Serializable]
public enum DevicePolicyManagerFlags {
	None = 0,
}
```

## Namespace Android.Drm

### Type Changed: Android.Drm.DrmManagerClient

Added methods:

```
public virtual DrmStoreObjectTypeCode GetDrmObjectType (string path, string mimeType);
	public virtual DrmStoreObjectTypeCode GetDrmObjectType (Android.Net.Uri uri, string mimeType);
```

## Namespace Android.Hardware.Location

### Type Changed: Android.Hardware.Location.GeofenceHardware

Removed fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceTransition enum directly instead of this field.")]
	public static const GeofenceTransition GeofenceEntered;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceError enum directly instead of this field.")]
	public static const GeofenceError GeofenceErrorIdExists;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceError enum directly instead of this field.")]
	public static const GeofenceError GeofenceErrorIdUnknown;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceError enum directly instead of this field.")]
	public static const GeofenceError GeofenceErrorInvalidTransition;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceError enum directly instead of this field.")]
	public static const GeofenceError GeofenceErrorTooManyGeofences;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceTransition enum directly instead of this field.")]
	public static const GeofenceTransition GeofenceExited;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceTransition enum directly instead of this field.")]
	public static const GeofenceTransition GeofenceFailure;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceTransition enum directly instead of this field.")]
	public static const GeofenceTransition GeofenceSuccess;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceTransition enum directly instead of this field.")]
	public static const GeofenceTransition GeofenceUncertain;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceMonitorStatus enum directly instead of this field.")]
	public static const GeofenceMonitorStatus MonitorCurrentlyAvailable;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceMonitorStatus enum directly instead of this field.")]
	public static const GeofenceMonitorStatus MonitorCurrentlyUnavailable;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceMonitoringType enum directly instead of this field.")]
	public static const GeofenceMonitoringType MonitoringTypeGpsHardware;

	[Obsolete ("This constant will be removed in the future version. Use Android.Hardware.Location.GeofenceMonitorStatus enum directly instead of this field.")]
	public static const GeofenceMonitorStatus MonitorUnsupported;
```

## Namespace Android.Media

### Type Changed: Android.Media.MediaMetadataRetriever

Added methods:

```
public string ExtractMetadata (int keyCode);
	public Android.Graphics.Bitmap GetFrameAtTime (long timeUs, int option);
```

### New Type Android.Media.AudioFlags

```
[Serializable]
public enum AudioFlags {
	None = 0,
}
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.PhoneNumberUtils

Added method:

```
public static string StringFromStringAndTOA (string s, int TOA);
```

## Namespace Android.Util

### Type Changed: Android.Util.Base64InputStream

Added constructor:

```
public Base64InputStream (System.IO.Stream in, int flags);
```

### Type Changed: Android.Util.Base64OutputStream

Added constructor:

```
public Base64OutputStream (System.IO.Stream out, int flags);
```

## Namespace Android.Views

### Type Changed: Android.Views.KeyCharacterMap

Added methods:

```
public int Get (Keycode keyCode, int metaState);
	public char GetMatch (Keycode keyCode, char[] chars, int metaState);
```

### Type Changed: Android.Views.KeyEvent

Added method:

```
public char GetMatch (char[] chars, int metaState);
```

### Type Changed: Android.Views.MotionEvent

Added methods:

```
public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, int[] pointerIds, MotionEvent.PointerCoords[] pointerCoords, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags, int source, int flags);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, float x, float y, MetaKeyStates metaState);
	public static MotionEvent Obtain (long downTime, long eventTime, int action, int pointers, float x, float y, float pressure, float size, MetaKeyStates metaState, float xPrecision, float yPrecision, int deviceId, Edge edgeFlags);
```

### Type Changed: Android.Views.View

Added method:

```
public void DispatchSystemUiVisibilityChanged (int visibility);
```

## Namespace Android.Views.InputMethods

### New Type Android.Views.InputMethods.CursorAnchorFlags

```
[Serializable]
public enum CursorAnchorFlags {
	None = 0,
}
```

## Namespace Java.Util

### Type Changed: Java.Util.EventListenerProxy

Removed property:

```
public virtual IEventListener Listener { get; }
```

Added property:

```
public virtual Java.Lang.Object Listener { get; }
```

## New Namespace Android.Media.Browse

### New Type Android.Media.Browse.MediaItemFlags

```
[Serializable]
public enum MediaItemFlags {
	None = 0,
}
```

## New Namespace Android.Media.Session

### New Type Android.Media.Session.MediaSessionFlags

```
[Serializable]
[Flags]
public enum MediaSessionFlags {
	None = 0,
}
```

## New Namespace Android.Service.Voice

### New Type Android.Service.Voice.RecognitionFlag

```
[Serializable]
public enum RecognitionFlag {
	None = 0,
}
```
