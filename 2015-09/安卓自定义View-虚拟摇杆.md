# Rocker
��׿����ҡ��
### ����΢��: [@��׿����ʦsloop](http://weibo.com/5459430586)
## [��ȡ���룺Rocker](https://github.com/GcsSloop/Rocker)

# ˵��
������Ҫ����һ������С���ƶ���Ӧ�ã�ʹ�ð������Ʋ�̫�������������һ������ҡ�ˡ�

��ҡ��ԭ��ʮ�ּ򵥣����Ǽ̳�һ��surfaceView��Ȼ������û����������ػ���棬ͬʱ���ظ��û���ǰ�Ƕȡ�
����û���ָ��ҡ�˱�����ҡ�ˣ���Ĭ�ϻ�������Բ�Σ�Ч������ͼ��ʾ��
<img src="http://img.blog.csdn.net/20150915193841817" width = "240" height = "450" alt="rocker3" align=center />  <img src="http://img.blog.csdn.net/20150915194048856" width = "240" height = "450" alt="rocker3" align=center />

 
ҡ�˵�ͼƬ�ͱ���ͼƬ��������ָ�������������й�����Ҳ���Ը�����ps��ͼƬ������ҪΪԲ���ұ���͸������ָ��ͼƬ��Ч�����£�

<img src="http://img.blog.csdn.net/20150915194120248" width = "240" height = "450" alt="rocker3" align=center />  <img src="http://img.blog.csdn.net/20150915194139505" width = "240" height = "450" alt="rocker3" align=center />

## <a href="http://pan.baidu.com/share/link?shareid=1802923607&uk=3009583694&fid=188394437825762" target="_blank">���������Թۿ�Ч����Ƶ</a>

 
# ʹ��ʾ����
## 1.�ڲ����ļ������ҡ��
 

     <com.sloop.widget.Rocker
         android:id="@+id/rudder"
         android:layout_width="match_parent"
         android:layout_height="match_parent" />

##  2.�ҵ��������ָ��ҡ��ͼƬ�ͱ���ͼƬ����ʡ�ԣ�
 
    Rocker rocker = (Rocker) findViewById(R.id.rudder);
		Bitmap rocker_bg = BitmapFactory.decodeResource(getResources(), R.drawable.rocker_bg1);
		Bitmap rocker_ctrl = BitmapFactory.decodeResource(getResources(), R.drawable.rocker_ctrl);
		rocker.setRockerBg(rocker_bg);
		rocker.setRockerCtrl(rocker_ctrl);
		
## 3.���ü��������ҡ��״̬

      rocker.setRudderListener(new Rocker.RudderListener() {
  			@Override
  			public void onSteeringWheelChanged(int action, int angle) {
  				if (action == Rocker.ACTION_RUDDER) {
  					//TODO:�¼�ʵ��
  					Log.e("�н�", "angle"+angle);
  				}
  			}
		});
		
# ������ò����ķ�����

    /** ����ҡ�˱���ͼ  */
    public void setRockerBg(Bitmap bitmap) {
        rocker_bg = Bitmap.createScaledBitmap(bitmap, mWheelRadius * 2, mWheelRadius * 2, true);
    }

    /** ����ҡ��ͼƬ */
    public void setRockerCtrl(Bitmap bitmap) {
        rocker_ctrl = Bitmap.createScaledBitmap(bitmap, mRudderRadius * 2, mRudderRadius * 2, true);
    }

    /** ����ҡ�˻�뾶  */
    public void setmWheelRadius(int radius) {
        mWheelRadius = DensityUtil.dip2px((ContextThemeWrapper) context, radius);
    }

    /** ����ҡ�˰뾶 */
    public void setmRudderRadius(int radius) {
        mRudderRadius = DensityUtil.dip2px((ContextThemeWrapper) context, radius);
    }

#### ps��ҡ��λ��Ĭ�ϴ���surfaceView�����ģ�������û���ṩ����ҡ��λ�õķ�����

### �ο������£� [android ����ҡ��ͼƬ��](http://blog.csdn.net/jwzhangjie/article/details/8839744)
### ����΢��: [@��׿����ʦsloop](http://weibo.com/5459430586)
## [��ȡ���룺Rocker](https://github.com/GcsSloop/Rocker)

