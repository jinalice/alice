����
ͨ���������˽����������õľ�����÷���

������	����	Ĭ��ֵ	����
id	string	null	��Χ����ѡ����
infinite	boolean	false	�Ƿ������ֲ���ѭ��
number	number	3	�������õ���������(ֻ��ѡ��3��5)
equalHeight	boolean	true	����numberΪ5ʱ,������������ڲ������Ƿ�ȸ�
prevOrNot	boolean	false	�Ƿ���ӵ��ʵ����һ��(����һ��)
nextOrNot	boolean	false	�Ƿ���ӵ��ʵ����һ��(����һ��)
dragOrNot	boolean	true	�Ƿ������ק����
clickOrNot	boolean	false	�������ͼƬ�˶�������,���ߵ��������a����������
dots	boolean	false	�Ƿ���ʾԲ�㰴ť
initCount	Object	{ set : false, initCountNumber : 0 }	set: �Ƿ��ʼ����һ��Ĭ��ͼƬ; initCountNumber : ��ʼ��ͼƬ��indexֵ
breakpoints	Object	{ set : false, width : 1024, number : 3 }	set: �Ƿ�ı���ʾͼƬ����; width: �ı������ٽ�ֵ; number: �ٽ�ֵʱͼƬ����
selfCalc	Object	{ set : false, secondScale : 0.75 }	set:�����ͼƬ�Ƿ���ֵ���(��opacity ͸��Ч��,�����ֵΪfalse); secondScale: ��������ͼƬ���ŵ�scaleֵ
addPcScroll	boolean	false	pc���Ƿ����ӹ����¼�
autoPlay	boolean	false	�Ƿ��Զ��ֲ�
autoPlayTime	number	1000	�Զ��ֲ����ʱ��(��λ:ms)
set3D	boolean	false	�Ƿ����3d���Ч��(����9,��10)
time	number	700	��λ��ms,�����ʼ���˶�����ʱ��
tabClass	string	is-active	��ǰ��������'li'������
leftClass	string	left	������ߵ�li����(���Ϊleft1,left2..)
rightClass	string	right	�����ұߵ�li����(���Ϊright1,right2..)
addClickClass	string	movecenter-click	clickOrNotΪtrueʱ,��Ҫ��ӵ�������� �� ���������a����������ʱ
scrollNumber	number	1	���prev��nextʱһ�����ֲ������ݸ���(Ĭ��Ϊ1,��ѡ��ʵ�ֶ�ͼ�ֲ�)
secondScale	number	0.5	�����������õ�scale��С(set3DΪtrueʱ,��ֵ���ɵ�)
minScale	number	0.5	������������ݵı���(��������ݱ�����Զ>=��ֵ)
moveDis	number	100	΢С�϶�ʱ,�೤����ʵ����һ�Ż���һ��(��λ:px)
notSetSize	boolean	false	���಻ϣ���ȱ�����,��ֵΪtrue,ͬʱsetSize����Ϊ�պ���
setSize	function	function(objParent,scale,oUl,self){
  if( $.browser.msie && $.browser.version<=8.0 ){
    var $obj = objParent.find('a');
    $obj.css( 'width' , scale*100+'%' );
    $obj.css( 'marginTop' , oUl.height()*(1-scale)/2 );
    $obj.css('opacity' , scale );
  }else{
    var $obj = objParent.find('a');
    $obj.css( 'transform' , 'scale('+scale+')' );
    $obj.css('opacity' , scale );
  } }	����scale����li��ǩ����������ʽ;setSize����Ϊ��ʱ��ʵ�ֵȸ��ֲ�Ч��
�������ṩ��һЩ������
prev(): �л�����һ��(��һ��)
next(): �л�����һ��(��һ��)
scroll( number , time ): ָ��ʱ�����л���ָ��������(ָ��������Ŵ�1��ʼ)
destroy(): ɾ�����


�������ṩ��һЩ�¼���
moveCenter-before: �˶���ʼ
moveCenter-after: �˶�����
moveCenter-next: ��� ��һ��/��һ��
moveCenter-prev��� ��һ��/��һ��
����ͨ��elem.on('�¼���',function( e , o){ } ) ��д�¼�����������
***���ܶ�li��������,�������е�position().left������
