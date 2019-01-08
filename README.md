# MayinTarlasi
MineFieldWithComputer
package mayinTarlasi.base;

public class MayinTarlasi {
	
	String [][]tarla = new String[10][10];
	String [][]mayinlar = new String[10][10];
	int xx=0;
	int yy=0;
	
	//tarla[Integer.parseInt(s.toCharArray()[0]+"")][Integer.parseInt(s.toCharArray()[1]+"")]="BOM";
	public void baslangic() {
		
		for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {tarla[i][j]=i+""+j;System.out.print(tarla[i][j]+"   ");}System.out.println();}
	
	
	int x=0;
	int y=0;
	for (int i=0; i<26; i++){
		x=(int)(Math.random()* 10);
		y=(int)(Math.random()* 10);
		
		if(mayinlar[x][y]==null) {mayinlar[x][y]="BOM";}else {i=i-1;}
		
		
		}
	System.out.print("ip ucu: "+x+""+y+" mayınlı. ");
	}
	
	public String oyun(String s) {
		int ii = Integer.parseInt(s.toCharArray()[0]+"");int jj = Integer.parseInt(s.toCharArray()[1]+"");
		
	if(mayinlar[ii][jj]=="BOM") {if(ii==xx&&jj==yy) {tarla[ii][jj]=mayinlar[ii][jj];for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {System.out.print(tarla[i][j]+"   ");}System.out.println();}System.out.println("bilgisayar "+xx+""+yy+" ile mayına bastı,kazandınız");}
	else{tarla[ii][jj]=mayinlar[ii][jj];for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {System.out.print(tarla[i][j]+"   ");}System.out.println();}System.out.println("mayına bastınız,kaybettiniz");}return "";}
	
		
	else{int sol=-1;int sag=1;int yukari =-1;int asagi =1;
	
	if(jj+sol>=0 && mayinlar[ii][jj+sol]=="BOM") {tarla[ii][jj]="!!";for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {System.out.print(tarla[i][j]+"   ");}System.out.println();}}
	
	else if(jj+sag<10 && mayinlar[ii][jj+sag]=="BOM") {tarla[ii][jj]="!!";for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {System.out.print(tarla[i][j]+"   ");}System.out.println();}}
	
	else if(ii+yukari>=0 && mayinlar[ii+yukari][jj]=="BOM") {tarla[ii][jj]="!!";for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {System.out.print(tarla[i][j]+"   ");}System.out.println();}}

	else if(ii+asagi<10 && mayinlar[ii+asagi][jj]=="BOM") {tarla[ii][jj]="!!";for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {System.out.print(tarla[i][j]+"   ");}System.out.println();}}
	
	else {tarla[ii][jj]="XX";for(int i =0;i<10;i++) {for(int j=0;j<10;j++) {System.out.print(tarla[i][j]+"   ");}System.out.println();}}
	
	
	}
	return s;
	}
	
	public  String pcrandom() {  
		xx=(int)(Math.random()* 10);
		yy=(int)(Math.random()* 10); return xx+""+yy;}
}
