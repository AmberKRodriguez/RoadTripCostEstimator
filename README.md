<h1>Road Trip Cost Estimator</h1>

<h2>Project Objectives:</h2>
<ul>
<li>Write a program that produces a road trip cost estimator with a GUI interface.</li>
<li>Using miles for distance, dollars per gallon for gasoline cost, and miles per gallon for gas mileage.</li>
</ul>


	Project3
	- distanceTitles: String[]           
	- gasolineCostTitles: String[]       
	- gasMileageTitles: String[]         
	- cboD: ComboBox<String>             
	- cboC: ComboBox<String>             
	- cboM: ComboBox<String>             
	- distanceField: TextField           
	- gasCostField: TextField            
	- gasMileageField: TextField         
	- hotelCostField: TextField          
	- foodCostField: TextField           
	- daysField: TextField               
	- attractionsField: TextField        
	- totalCostField: TextField   

	javafx.scene.layout.GridPane
	-alignment: ObjectProperty
	-gridLinesVisible: BooleanProperty
	-hgap: DoubleProperty
	-vgap: DoubleProperty
	+GridPane()
	+add(child: Node, columnIndex: int, rowIndex: int): void
	+addColumn(columnIndex: int, children: Node...): void
	+addRow(rowIndex: int, children: Node...): void
	+getColumnIndex(child: Node): int
	+setColumnIndex(child: Node, columnIndex: int): void
	+getRowIndex(child: Node): int
	+setRowIndex(child: Node, rowIndex: int): void
	+setHalighnment(child: Node, value: HPos): void
	+setValighnment(child: Node, value: VPos): void

<h3>Steps taken:</h3> 	
<ol>
 <li>Created a grid pane and set its properties</li>
 <li>Set alignment of nods within pane</li>
 <li>Set Horizontal & vertical gaps between nodes</li>
 <li>Place nodes in the pane</li>
	 <ul>
		 <li>0,0 Distance Label node – 1,0 Distance (input) textField node – 2,0 Miles/kilometers Cost ComboBox node</li>
		 <li>0,1 Gasoline Cost Label – 1,1 Gasoline Cost (input) textField node – 2,1 Dollars per gallon/dollars per liter ComboBox node</li>
		 <li>0,2 gas mileage Label node – 1,2 gas mileage (input) textField node – 2,2 miles per gallon/ kilometers per liter ComboBox node</li>
		 <li>0,3 Number of Days Label node – 1,3 Number of Days (input) textField node</li>
		 <li>0,4 Hotel Cost Label node – 1,4 Hotel Cost (input) textField node</li>
		 <li>0,5 Food Cost Label node – 1,5 Food Cost (input) textField node</li>
		 <li>0,6 Attractions Label node -1,6 Attractions (input) textField node</li>
		 <li>0,7 Button node ”Calculate” – 1,7 setOnAction to output totalCost</li>
		 <li>0,8 Total Trip Cost Label node – 0,8 Total Trip Cost(output) textField node does not take in input</li>
	</ul>

<li>Create scene and place it in the stage ( Title: Trip Cost Estimator)</li>
<li>Method calculateTotalCost()</li>
	<ul>
		<li>Convert numerical strings into Doubles and return string that describes each key code (getText())</li>
		<li>Distance, gasCost, gasMileage, hotelCost, foodCost, days, attractions, totalGasolineCost, totalTripCost.</li>
	</ul>
<li>Include mesument conversions for :</li>
	<ul>	
 		<li>kilometers</li>
		<li>dollars/liter</li>
		<li>kilometers/liter</li>
	</ul>
 <li>Add calculations to get total trip cost </li>
 		<ul><li>gasoline cost = 𝑑𝑖𝑠𝑡𝑎𝑛𝑐𝑒 𝑔𝑎𝑠 𝑚𝑖𝑙𝑎𝑔𝑒 –  gasoline cost total trip cost = gasoline cost + (hotel cost + food cost)  number of days + attractions</li></ul>

 </ol>

	

