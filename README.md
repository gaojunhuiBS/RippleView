
RippleView
===============

A simple ripple view for Android


-----


![](https://github.com/ruzhan123/RippleView/raw/master/gif/ripple.gif)




RippleView use **Animation** change circle radius draw circle

[![](https://jitpack.io/v/ruzhan123/RippleView.svg)](https://jitpack.io/#ruzhan123/RippleView)

Gradle
------

Add it in your root build.gradle at the end of repositories:


```java

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

Add the dependency:


```java

	dependencies {
	         compile 'com.github.ruzhan123:RippleView:v1.0'
	}
```

Usage
-----

```xml

	<zhan.rippleview.RippleView
	    android:id="@+id/root_rv"
	    app:radius="200"
	    app:stroke_width="1"
	    app:duration="3000"
	    app:repeat_count="1"
	    app:two_ripple_times="1.5"
	    app:three_ripple_times="2.0"
	    app:max_more_radius_times="1.5"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent" />
```

expend
-------


```java

	public interface RippleAnimationListener {
	
	void onAnimationUpdate(ValueAnimator animation);
	
	void onAnimationStart(Animator animation);
	
	void onAnimationEnd(Animator animation);
	
	void onAnimationCancel(Animator animation);
	
	void onAnimationRepeat(Animator animation);
	}

	public void setRippleStateListener(RippleAnimationListener listener) {
	if (!mRippleAnimationListeners.contains(listener)) {
	  mRippleAnimationListeners.add(listener);
	}
	}
	
	public void removeRippleStateListener(RippleAnimationListener listener) {
	if (mRippleAnimationListeners.contains(listener)) {
	  mRippleAnimationListeners.remove(listener);
	}
	}
	
	public void removeRippleStateListenerAll() {
	mRippleAnimationListeners.clear();
	}
```

```java

	public void setRadius(int radius) {
	mRadius = radius;
	mChangeRadius = radius;
	}
	
	public void setStrokeWidth(int strokeWidth) {
	mStrokeWidth = strokeWidth;
	}
	
	public void setDuration(int duration) {
	mDuration = duration;
	}
	
	public void setRepeatCount(int repeatCount) {
	mRepeatCount = repeatCount;
	}
	
	public void setCirclePoint(float x, float y) {
	mCx = x;
	mCy = y;
	}
	
	public void setOutStrokePaintColor(int color) {
	mOutStrokePaint.setColor(color);
	}
	
	public void setInStrokePaintColor(int color) {
	mInStrokePaint.setColor(color);
	}
	
	public void setInPaintColor(int color) {
	mInPaint.setColor(color);
	}
	
	public void setInterpolator(Interpolator interpolator) {
	mInterpolator = interpolator;
	}
	
	public void setTwoRippleTimes(float times) {
	mTwoRippleTimes = times;
	}
	
	public float getTwoRippleTimes() {
	return mTwoRippleTimes;
	}
	
	public void setThreeRippleTimes(float times) {
	mThreeRippleTimes = times;
	}
	
	public float getThreeRippleTimes() {
	return mThreeRippleTimes;
	}

```

Developed by
-------

 ruzhan - <a href='javascript:'>ruzhan333@gmail.com</a>


License
-------

    Copyright 2017 ruzhan

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
