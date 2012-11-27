College-projects
================

/*Computer Graphics*/

/*Program to draw a line using DDA Algorithm*/

#include<stdio.h>
#include<conio.h>
#include<math.h>
#include<graphics.h>

void main()
{
int i,x,y,xa,xb,ya,yb,steps,xinc,yinc,dx,dy;
int gdriver=DETECT,gmode;
initgraph(&gdriver,&gmode,"c:\\tc\\bgi");
printf("Enter the X and Y co-ordinates: \n");
scanf("%d%d%d%d",&xa,&xb,&ya,&yb);
dx=xb-xa;
dy=yb-ya;
if(abs(dx)>abs(dy))
{
steps=abs(dx);
}
else
{
steps=abs(dy);
}
xinc=dx/steps;
yinc=dy/steps;
x=xa;
y=ya;
putpixel(floor(x),floor(y),100);
for(i=0;i<=steps;i++)
{
x+=xinc;
y+=yinc;
putpixel(floor(x),floor(y),100);
}
getch();
}