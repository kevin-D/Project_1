Project_1
=========
#include"stdio.h"
typedef struct 
{
	int x;
	int y;
}POINT;
/
点相等判定
 参数p1：第一点；p2：第二点
 返回1：相等；0：不想等
/
int equals(POINT p1,POINT p2)
{
	return p1.x==p2.x && p1.y==p2.y;
}
/
判定点是否构成三角形
参数points:3个点构成的数组
返回1：构成三角形；0：不构成三角形
/
int triangle(POINT point[])
{
	if(equals(points[0],points[1]) || (equals(points[0],points[2]) || equals(points[1],point[2]))
		return 0;
	if(point[0].x-points[1].x==0)
	{
		return points[2].x!=point[1].x;
	}
	else{
		return point[2].y-points[1].y!=(points[0].y-points[1].y)/(points[0].x-points[1].x)*(points[2].x-points[1].x);
	}
}
int main(int argc, char* argv[]}
{
	POINT points1[]={{1,2},{4,5},{6,3}};
	POINT points2[]={{1,1},{1,5},{1,3}};
	POINT points3[]={{1,2},{4,2},{6,2}};
	POINT points4[]={{1,2},{4,8},{6,12}};
	printf("%d ",triangle(points1));
	printf("%d ",triangle(points2));
	printf("%d ",triangle(points3));
	printf("%d ",triangle(points4));
}
