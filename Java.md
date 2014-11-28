


http://www.developer.com/tech/article.php/3669436/Test-Driving-a-Java-Command-Line-Application.htm


<build>
  <plugins>
    <plugin>
      <artifactId>maven-assembly-plugin</artifactId>
      <configuration>
        <archive>
          <manifest>
            <mainClass>fully.qualified.MainClass</mainClass>
          </manifest>
        </archive>
        <descriptorRefs>
          <descriptorRef>jar-with-dependencies</descriptorRef>
        </descriptorRefs>
      </configuration>
    </plugin>
  </plugins>
</build>


mvn clean compile assembly:single
mvn install


org.apache.commons.lang3.StringEscapeUtils


"1" "11" "23.4" "555" "employee(Joshua,Ames,22.0)" "aa" "banana" "jonas" "zabumba"

java -cp javatest-0.0.1-SNAPSHOT-jar-with-dependencies.jar com.shirashiki.javatest.JavaTestApp opConcatenate "I would " "love to " "work at " M c G i l l



java -cp javatest-0.0.1-SNAPSHOT-jar-with-dependencies.jar com.shirashiki.javatest.JavaTestApp opConcatenate "I would " "love to " "work at " M c G i l l
I would love to work at McGill


java -cp javatest-0.0.1-SNAPSHOT-jar-with-dependencies.jar com.shirashiki.javatest.JavaTestApp opConcatenate I would love to work at McGill


java -cp javatest-0.0.1-SNAPSHOT-jar-with-dependencies.jar com.shirashiki.javatest.JavaTestApp opSortAsc employee\(Stephan,Zweig,22000\) Zabumba Ball Apple 1.1 1 2.12 2.1 2 employee\(Joshua,Ames,22000\)


"1" "1.1" "2" "2.1" "2.12" "employee(Joshua,Ames,22000.0)" "Apple" "Ball" "Zabumba" "employee(Stephan,Zweig,22000.0)" 

