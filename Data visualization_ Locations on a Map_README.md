- 👋 Hi, I’m @spmaniraj
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
spmaniraj/thamizhamuthu R is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
PImage mapImage;
Table locationTable;
int rowCount;
void setup( ) {
size(640, 400);
mapImage = loadImage("Downloads/map.png");
locationTable = new Table("Downloads/locations.tsv");
rowCount = locationTable.getRowCount( );
}
void draw( ) {
background(255);
image(mapImage, 0, 0);
smooth( );
fill(192, 0, 0);
noStroke( );
for (int row = 0; row < rowCount; row++) {
float x = locationTable.getFloat(row, 1);
float y = locationTable.getFloat(row, 2);
ellipse(x, y, 9, 9);
}
}
![image](https://user-images.githubusercontent.com/106227601/170669529-e8de6590-372d-4aec-b321-334e3e83f623.png)
