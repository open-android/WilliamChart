# WilliamChart项目使用

开源地址：[https://github.com/open-android/WilliamChart](https://github.com/open-android/WilliamChart "https://github.com/open-android/WilliamChart")

# 运行效果

![](screenshot.gif)

## 使用步骤

### 1. 在project的build.gradle添加如下代码(如下图)

	allprojects {
	    repositories {
	        maven { url "https://jitpack.io" }
	    }
	}

![](build.gradle2.png)

### 2. 在Module的build.gradle添加依赖

    compile 'com.github.open-android:WilliamChart:v2.4.0'


### 3.布局文件使用

	<com.db.chart.view.LineChartView
	    android:id="@+id/chart"
	    app:chart_axisColor="#30547d99"
	    android:layout_width="match_parent"
	    android:layout_height="match_parent"
	    android:layout_centerHorizontal="true"
	    android:layout_marginTop="23dp" />

### 4.Activity初始化

 	mChart = (LineChartView) findViewById(R.id.chart);

    LineSet dataset = new LineSet(mLabels, mValues[0]);
    //...省略部分代码，请参考mobile中事例
    mChart.addData(dataset);//设置数据


    mChart.show();//显示
	

	


	
