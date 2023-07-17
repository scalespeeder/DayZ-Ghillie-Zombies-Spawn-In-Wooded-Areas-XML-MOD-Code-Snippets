DAYZ CHERNARUS & LIVONIA Ghillie Suit Infected Zombies Spawning In Wooded Areas & Countryside xml Mod Code Snippets Changelog & Terms Of Use

Will work on PC & Console Community Servers.

Limited Testing on PC Chernarus & Livonia Local PC Server DAYZ  Version 1.21 July 2023.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml code snippets could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded xml code snippets neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these code snippets to ensure proper
functioning of your server.

==========================

Ghillie Suit Zombies That Spawn In The Countryside!


In Cfgspawnabletypes, edit the ZmbM_PatrolNormal_Autumn as below.

<type name="ZmbM_PatrolNormal_Autumn">
		<cargo preset="foodArmy" />
		<cargo preset="ammoArmy" />
		<attachments preset="glasses2Army" /><!--headtorch-->
		<attachments preset="hats2Army" /><!--ghillie hat-->
		<attachments preset="bags2Army" /><!--ghillie suit-->
		<attachments preset="vestsArmy" />
	</type>
	
REMEMBER TO SAVE!
	
In cfgrandompresets, add this:

	<attachments chance="1.0" name="bags2Army">
		<item name="GhillieSuit_Woodland" chance="1.0" />
		</attachments>
		
		<attachments chance="1.0" name="hats2Army">
			<item name="GhillieHood_Woodland" chance="1.0" />
		</attachments>
		
		<attachments chance="1.0" name="glasses2Army">
			<item name="Headtorch_Black" chance="0.25" />
			<item name="Headtorch_Grey" chance="0.25" />
		</attachments>
		
REMEMBER TO SAVE!
		
In Events, add this:

<event name="InfectedGhillie">
        <nominal>50</nominal>
        <min>25</min>
        <max>100</max>
        <lifetime>3</lifetime>
        <restock>0</restock>
        <saferadius>100</saferadius>
        <distanceradius>50</distanceradius>
        <cleanupradius>100</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>player</position>
        <limit>custom</limit>
        <active>1</active>
        <children>
            <child lootmax="5" lootmin="0" max="0" min="100" type="ZmbM_PatrolNormal_Autumn"/>
        </children>
    </event>
	
REMEMBER TO SAVE!
	
Optional: Remove ZmbM_PatrolNormal_Autumn from all other infected events, so Ghillie Zombies aren't in normal military locations.
	
In CHERNARUS Zombie Territories Add:

<!--this uses EVERY OTHER deer spawn point-->

 <territory color="1136576269"> 
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="327.501" z="10522.5" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="525.001" z="9245" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1087.5" z="9160" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="342.501" z="9807.5" r="142.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="457.501" z="14401.3" r="165"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1998.75" z="12953.8" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="725.001" z="13571.3" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10871.5" z="8655" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11842" z="8352.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12060.1" z="8290.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11731.5" z="8814.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="6192.5" z="6182.86" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5995" z="6937.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7029.64" z="7317.86" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5772.5" z="6785" r="135"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11397.5" z="5145.63" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10365" z="6063.13" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11692" z="5129.32" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11278.6" z="5675.13" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12350" z="5476.87" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12708.8" z="5602.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12473.1" z="5976.25" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13338.1" z="5012.75" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12758.1" z="5155.88" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12777.5" z="4954" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12341.3" z="5295.25" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9750.63" z="14674.4" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10393.1" z="14221.9" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9780.63" z="15179.4" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="492.501" z="8130" r="105"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="888.751" z="6928.75" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="776.251" z="6133.75" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="240.001" z="7806.25" r="135"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="310.001" z="5585" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="457.501" z="5005" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="892.501" z="4717.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7682.36" z="11717.5" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7393.07" z="10733.2" r="150"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7037.29" z="10861.5" r="157.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7690.21" z="11128.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2210" z="12665" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1645" z="12500" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2107.5" z="12610" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8752.5" z="12380.6" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9500.63" z="11911.9" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9536.25" z="12153.8" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9316.88" z="12050.6" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9747.5" z="3661.88" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9765" z="4473.13" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9993.75" z="4225.63" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9809.73" z="3836.34" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9248.75" z="10447.3" r="150"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10333.5" z="10182.8" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8362.5" z="9978.75" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7554.89" z="9269.89" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8820" z="10706.3" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="653.251" z="2859" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="352.751" z="3810.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="745.751" z="3180" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2888.75" z="2416.25" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3951.25" z="3026.25" r="130"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3773.13" z="3109.38" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3556.25" z="3061.25" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1034.5" z="11280" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="541.001" z="10806.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1793.88" z="11295.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1572" z="10896" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="552.5" z="1977.5" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1275" z="2447.5" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1137.5" z="2622.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11628" z="3761.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10876.1" z="3474" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11668" z="3961.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1227.5" z="7705" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1402.5" z="7437.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2151" z="7536.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9355.36" z="7175.36" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9245" z="8255.71" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8856.88" z="8336.76" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9733.33" z="7914.88" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13829.4" z="14435" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13334.4" z="14472.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="14176.3" z="14508.1" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="14937.5" z="14243.8" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10400" z="6693.75" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10013.1" z="6683.13" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10130" z="6967.5" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11041" z="11221.3" r="127.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10617.5" z="10838.8" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12124.5" z="11135.8" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9633.5" z="12599.3" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10415.5" z="11667.8" r="105"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9680.42" z="6236.46" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9219.17" z="4905" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8911.67" z="5691.67" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7787.32" z="4477.68" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7686.25" z="4015.89" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8560" z="4447.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2736.75" z="13703.5" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2646.25" z="13837.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2844.75" z="13877" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2204.75" z="13797" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8187.32" z="5064.64" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7680.54" z="5475.71" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8347.32" z="5847.86" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12667" z="5842" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11837" z="6326" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11680" z="6507" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12110" z="5832.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4610.71" z="3111.07" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5139.64" z="4082.86" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5167.14" z="3072.14" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8904.14" z="6451.71" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8735.57" z="6367.43" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8447.36" z="6355.64" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8583.79" z="6890.64" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8870.21" z="6956.36" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7659" z="5448" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7846.5" z="5669.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8060" z="5955.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4572.86" z="5949.64" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4998.93" z="5100" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5287.14" z="4894.64" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5385" z="5705" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11637.5" z="4485" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12090" z="4575" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12677.5" z="4550" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11547.5" z="4710" r="80"/>
    </territory>	
 
 REMEMBER TO SAVE!
 OR
 
 <!--this uses EVERY deer spawn point, could cause deer not to spawn-->
 
 <territory color="1136576269"> 
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="327.501" z="10522.5" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="422.501" z="9905" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="525.001" z="9245" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="117.5" z="10287.5" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1087.5" z="9160" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="632.5" z="9327.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="342.501" z="9807.5" r="142.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="438.751" z="12953.8" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="457.501" z="14401.3" r="165"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1260" z="13055" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1998.75" z="12953.8" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1161.25" z="13383.8" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="725.001" z="13571.3" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="525.001" z="13272.5" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10871.5" z="8655" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11431.5" z="9227" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11842" z="8352.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12007.7" z="9630.67" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12060.1" z="8290.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11463" z="8859.38" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11731.5" z="8814.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="6234.29" z="6596.79" r="135"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="6192.5" z="6182.86" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="6057.5" z="6093.93" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5995" z="6937.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="6842.5" z="7222.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7029.64" z="7317.86" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="6747.86" z="6773.93" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5772.5" z="6785" r="135"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11162.5" z="5115" r="142.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11397.5" z="5145.63" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10676.9" z="5218.13" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10365" z="6063.13" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11068.1" z="4890" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11692" z="5129.32" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11826.3" z="5120.63" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11278.6" z="5675.13" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11845" z="5767.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12350" z="5476.87" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12218.1" z="5437.5" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12708.8" z="5602.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12413.1" z="5330.62" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12473.1" z="5976.25" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11656" z="5365.09" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13338.1" z="5012.75" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12135.6" z="5429.63" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12758.1" z="5155.88" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12873.8" z="5305.25" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12777.5" z="4954" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12370.6" z="5313.38" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12341.3" z="5295.25" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9940.63" z="14109.4" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9750.63" z="14674.4" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9860.63" z="14181.9" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10393.1" z="14221.9" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9835.63" z="14546.9" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9780.63" z="15179.4" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="353.394" z="6498.21" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="492.501" z="8130" r="105"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="584.465" z="7417.5" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="888.751" z="6928.75" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="600.001" z="7146.25" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="776.251" z="6133.75" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="673.394" z="6020.18" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="240.001" z="7806.25" r="135"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="337.5" z="5010" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="310.001" z="5585" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="875.001" z="5337.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="457.501" z="5005" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="240.001" z="4935" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="892.501" z="4717.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="320" z="5465" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7682.36" z="11717.5" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7587" z="11652.4" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7393.07" z="10733.2" r="150"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8206.17" z="11838.9" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7037.29" z="10861.5" r="157.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7699.06" z="10959.6" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7690.21" z="11128.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7719.42" z="11577.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2210" z="12665" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="312.5" z="12545" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1645" z="12500" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2105" z="12737.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2107.5" z="12610" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1065" z="12420" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8752.5" z="12380.6" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8754.38" z="12136.9" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9500.63" z="11911.9" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9813.75" z="11765.6" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9536.25" z="12153.8" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8833.13" z="12350.6" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9316.88" z="12050.6" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9088.13" z="12403.1" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9747.5" z="3661.88" r="90"/>
		<zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10016.9" z="3180" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9765" z="4473.13" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10163.8" z="3226.88" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9993.75" z="4225.63" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9878.13" z="3481.25" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9809.73" z="3836.34" r="90"/>
		<zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10026" z="9880.25" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9248.75" z="10447.3" r="150"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9934" z="9580.25" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10333.5" z="10182.8" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8862.5" z="10528.8" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8362.5" z="9978.75" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9232.5" z="10214.8" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7554.89" z="9269.89" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9184" z="9864.25" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8820" z="10706.3" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="114.25" z="4382" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="653.251" z="2859" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="203.251" z="3619" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="352.751" z="3810.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="338.251" z="2985.5" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="745.751" z="3180" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="400.75" z="3003" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2888.75" z="2416.25" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3156.25" z="2363.75" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3951.25" z="3026.25" r="130"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3808.75" z="2941.25" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3773.13" z="3109.38" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2716.25" z="2521.25" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3556.25" z="3061.25" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3672.5" z="3017.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1034.5" z="11280" r="67.5"/>
		<zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="900.501" z="10756" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="541.001" z="10806.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1665.5" z="10723.5" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1793.88" z="11295.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1052.5" z="10886.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1572" z="10896" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="485.001" z="2377.5" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="552.5" z="1977.5" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="665.001" z="2277.5" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1275" z="2447.5" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="182.501" z="2620" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1137.5" z="2622.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1512.5" z="2447.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11628" z="3761.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10196.8" z="3192.75" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10876.1" z="3474" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10729.9" z="3612.12" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11668" z="3961.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10929.3" z="4276.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1227.5" z="7705" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1277.5" z="7612.5" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1402.5" z="7437.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1040" z="7397.5" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2151" z="7536.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1352.5" z="7975" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9355.36" z="7175.36" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9387.5" z="7688.21" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9245" z="8255.71" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9805" z="7591.55" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8856.88" z="8336.76" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9632.5" z="8297.38" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9733.33" z="7914.88" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9303.33" z="7081.55" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13829.4" z="14435" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13683.1" z="14423.8" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13334.4" z="14472.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="13341.9" z="14568.1" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="14176.3" z="14508.1" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="14448.1" z="14420" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="14937.5" z="14243.8" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10930.4" z="6432.86" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10400" z="6693.75" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10075" z="6405" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10013.1" z="6683.13" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11152.5" z="6804.64" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10130" z="6967.5" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10171.3" z="6766.25" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11041" z="11221.3" r="127.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10719" z="10992.8" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10617.5" z="10838.8" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11482" z="11779.3" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12124.5" z="11135.8" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10785.5" z="11743.8" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9633.5" z="12599.3" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10560" z="11268.8" r="135"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10415.5" z="11667.8" r="105"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8829.17" z="6084.17" r="142.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9680.42" z="6236.46" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8914.17" z="4962.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9219.17" z="4905" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9981.67" z="5863.33" r="165"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8911.67" z="5691.67" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8857.5" z="4132.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7787.32" z="4477.68" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8044.82" z="4534.11" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7686.25" z="4015.89" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="6824.47" z="4549.46" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8560" z="4447.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7024.11" z="4627.32" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2736.75" z="13703.5" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2994.75" z="13599.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2646.25" z="13837.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2336.25" z="14471" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2844.75" z="13877" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2387.25" z="14219.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2204.75" z="13797" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2964.75" z="14449.5" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8187.32" z="5064.64" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8310.54" z="5298.93" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7680.54" z="5475.71" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7763.39" z="4939.29" r="75"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8347.32" z="5847.86" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8063.39" z="5427.14" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12667" z="5842" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12930.5" z="5862.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11837" z="6326" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12209" z="5549.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11680" z="6507" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12175" z="6685" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12110" z="5832.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4901.43" z="3239.29" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4610.71" z="3111.07" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4902.86" z="3834.29" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5139.64" z="4082.86" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4844.29" z="2989.64" r="52.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5167.14" z="3072.14" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4907.14" z="4234.64" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8904.14" z="6451.71" r="97.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7518.88" z="6823.5" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8735.57" z="6367.43" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8139.5" z="6772.25" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8447.36" z="6355.64" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8694.14" z="6895.29" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8583.79" z="6890.64" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7670.75" z="6579.13" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8870.21" z="6956.36" r="112.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7245" z="6040.5" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7659" z="5448" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8124.17" z="5821.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7846.5" z="5669.5" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8429.5" z="6136.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8060" z="5955.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4088.57" z="6087.86" r="105"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4572.86" z="5949.64" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4077.5" z="5951.07" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4998.93" z="5100" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5192.14" z="4730.36" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5287.14" z="4894.64" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4842.5" z="5181.79" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5385" z="5705" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12450" z="4427.5" r="110"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11637.5" z="4485" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12550" z="4610" r="82.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12090" z="4575" r="67.5"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12760" z="4932.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12677.5" z="4550" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11547.5" z="4710" r="80"/>
    </territory>	
	
REMEMBER TO SAVE!

In LIVONIA Zombie Territories Add:

<!--This uses EVERY OTHER deer spawn point-->

<territory color="1136576269">
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10537.5" z="1683.33" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10514.6" z="2504.17" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10935.4" z="1997.92" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9339.59" z="1108.33" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10153.6" z="904.666" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9877.61" z="1022.47" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1877.08" z="4535" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1323.21" z="4638.69" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2141.67" z="4160.42" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4422.92" z="3040.63" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3340.63" z="2618.75" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3837.5" z="3272.5" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2125" z="934.4" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2609.38" z="1678.15" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2478.13" z="1396.9" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5325.63" z="836.25" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5800" z="1467.5" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7602.08" z="3385.43" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7031.25" z="3168.8" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7008.33" z="2647.87" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2512.5" z="1998.21" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2501.79" z="925" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9370" z="3444.06" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9070" z="4000" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10096.9" z="3194.38" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11977.5" z="12470" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10857.5" z="12190" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2037.5" z="3397.92" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2556.25" z="3552.08" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1437.5" z="2945.83" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="460.417" z="6945.83" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="943.75" z="6331.25" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="952.5" z="6572.5" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9886.61" z="486.83" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10754.2" z="325" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10531.3" z="703.125" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11931.3" z="3663.75" r="130"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12113.8" z="3790" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12553.1" z="2535" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11085.4" z="6069.79" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11075" z="5295.83" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10693.8" z="5189.58" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="772.619" z="11907.2" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="542.956" z="11532.7" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12164.8" z="2486.67" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11790.6" z="2333.75" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11592.9" z="1965.02" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3285" z="577.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3960" z="1450" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4660" z="950" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8134.69" z="5086.88" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8823.13" z="5416.25" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9355" z="4535" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1695" z="767.5" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1195" z="1050" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="545" z="775" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12609.6" z="6945" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12043.8" z="7047.89" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12312.5" z="7802.08" r="140"/>
    </territory>

REMEMBER TO SAVE!

OR

<!--This uses EVERY deer spawn point, could cause deer not to spawn-->

<territory color="1136576269">
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10537.5" z="1683.33" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10965.4" z="2224.17" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10514.6" z="2504.17" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10977.1" z="2395.83" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10935.4" z="1997.92" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9871.25" z="1515" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9339.59" z="1108.33" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9647.4" z="1109.37" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10153.6" z="904.666" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10730" z="985.366" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9877.61" z="1022.47" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10527.1" z="1397.93" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1877.08" z="4535" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2034.17" z="4542.5" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1323.21" z="4638.69" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1743.75" z="4331.25" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2141.67" z="4160.42" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3778.13" z="2956.25" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4422.92" z="3040.63" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4059.38" z="2925" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3340.63" z="2618.75" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3075" z="3109.38" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3837.5" z="3272.5" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3880" z="2540" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2125" z="934.4" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2715.63" z="690.65" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2609.38" z="1678.15" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2873.96" z="1484.4" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2478.13" z="1396.9" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5665" z="1780" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5325.63" z="836.25" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5435" z="1387.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5800" z="1467.5" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="5214.38" z="1133.54" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7602.08" z="3385.43" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7043.75" z="2947.87" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7031.25" z="3168.8" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8053.13" z="3274" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="7008.33" z="2647.87" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2430.36" z="1282.14" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2512.5" z="1998.21" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2119.64" z="1741.07" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2501.79" z="925" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2889.29" z="1785.71" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9370" z="3444.06" r="50"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9643.44" z="3554.06" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9070" z="4000" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9837.5" z="3317.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10096.9" z="3194.38" r="70"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12040" z="11962.5" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11977.5" z="12470" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11192.5" z="12380" r="90"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10857.5" z="12190" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11325" z="12480" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2037.5" z="3397.92" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1556.25" z="3337.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2556.25" z="3552.08" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2260.42" z="3281.25" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1437.5" z="2945.83" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="283.333" z="7016.67" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="460.417" z="6945.83" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="172.917" z="6745.83" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="943.75" z="6331.25" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1568.75" z="6516.67" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="952.5" z="6572.5" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10784.4" z="878.125" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9886.61" z="486.83" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10425.9" z="910.938" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10754.2" z="325" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10969.4" z="260.491" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10531.3" z="703.125" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12573.1" z="3168.75" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11931.3" z="3663.75" r="130"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11806.3" z="3265.31" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12113.8" z="3790" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12101.3" z="3075.63" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12553.1" z="2535" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10195.8" z="5843.75" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11085.4" z="6069.79" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11325" z="5487.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11075" z="5295.83" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10741.7" z="5060.42" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="10693.8" z="5189.58" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1461.45" z="11327.4" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="772.619" z="11907.2" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="337.505" z="11786.9" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="542.956" z="11532.7" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1692.71" z="11427.1" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12164.8" z="2486.67" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12065.2" z="2075.89" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11790.6" z="2333.75" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11849.1" z="1691.76" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11592.9" z="1965.02" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3425" z="805" r="60"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3285" z="577.5" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3170" z="1010" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="3960" z="1450" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4022.5" z="1065" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="4660" z="950" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8058.13" z="5412.19" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8134.69" z="5086.88" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9187.5" z="5852.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="8823.13" z="5416.25" r="160"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9695" z="5112.5" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="9355" z="4535" r="120"/>
		<zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1300" z="847.5" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1695" z="767.5" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1537.5" z="1145" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="1195" z="1050" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="2030" z="1345" r="80"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="545" z="775" r="100"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11664.2" z="7543.11" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12609.6" z="6945" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="11993.8" z="7532.28" r="120"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12043.8" z="7047.89" r="140"/>
        <zone name="InfectedGhillie" smin="0" smax="0" dmin="1" dmax="2" x="12312.5" z="7802.08" r="140"/>
    </territory>
	
REMEMBER TO SAVE!


Restart your server, and you should be good to go!

Good luck, Rob.