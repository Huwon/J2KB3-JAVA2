<h1 id="toc_0">[3단계] for문</h1>

<ul>
<li>백준 알고리즘에서는 <strong><em>&quot;클래스명&quot;</em></strong>을 <strong><em>&quot;Main&quot;</em></strong>으로 해주어야 한다!</li>
<li>&quot;<strong>BufferedReader</strong>&quot;, &quot;<strong>BufferedWriter</strong>&quot;, 그리고 &quot;<strong>StringTokenize</strong>&quot;에 대한 자세한 내용은 따로 정리해서 업로드 할 예정!</li>
</ul>

<h2 id="toc_1">1. [1330번] 두 수 비교하기</h2>

<h3 id="toc_2">문제</h3>

<div><pre><code class="language-none">N을 입력받은 뒤, 구구단 N단을 출력하는 프로그램을 작성하시오. 출력 형식에 맞춰서 출력하면 된다.</code></pre></div>

<h3 id="toc_3">입력</h3>

<div><pre><code class="language-none">첫째 줄에 N이 주어진다. N은 1보다 크거나 같고, 9보다 작거나 같다.</code></pre></div>

<h3 id="toc_4">출력</h3>

<div><pre><code class="language-none">출력형식과 같게 N*1부터 N*9까지 출력한다.</code></pre></div>

<h3 id="toc_5">예제 입력 1</h3>

<p><code>2</code></p>

<h3 id="toc_6">예제 출력 1</h3>

<div><pre><code class="language-none">2 * 1 = 2
2 * 2 = 4
2 * 3 = 6
2 * 4 = 8
2 * 5 = 10
2 * 6 = 12
2 * 7 = 14
2 * 8 = 16
2 * 9 = 18</code></pre></div>

<h3 id="toc_7">내 제출 코드</h3>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int N = in.nextInt();

        for(int i = 0; i &lt; 9; i++)
        {
            System.out.println(N + &quot; * &quot; + (i+1) + &quot; = &quot; + (N*(i+1)));
            //System.out.printf(&quot;%d * %d = %d\n&quot;,N,(i+1), N*(i+1));도 가능!
        }

        in.close();
    }
}</code></pre></div>

<ul>
<li><code>printf</code>와 <code>println</code> 중 문제에서 더 쉽게 쓰일 수 있는 걸 골라 쓰면 된다.</li>
</ul>

<h2 id="toc_8">2. [10950번] A + B - 3</h2>

<h3 id="toc_9">문제</h3>

<div><pre><code class="language-none">두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.</code></pre></div>

<h3 id="toc_10">입력</h3>

<div><pre><code class="language-none">첫째 줄에 테스트 케이스의 개수 T가 주어진다.

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 &lt; A, B &lt; 10)</code></pre></div>

<h3 id="toc_11">출력</h3>

<div><pre><code class="language-none">각 테스트 케이스마다 A+B를 출력한다.</code></pre></div>

<h3 id="toc_12">예제 입력 1</h3>

<div><pre><code class="language-none">5
1 1
2 3
3 4
9 8
5 2</code></pre></div>

<h3 id="toc_13">예제 출력 1</h3>

<div><pre><code class="language-none">2
5
7
17
7    </code></pre></div>

<h3 id="toc_14">내 제출 코드</h3>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int T = in.nextInt();

        for(int i = 0; i &lt; T; i++)
        {
            int A = in.nextInt();
            int B = in.nextInt();
            System.out.println((A+B));
        }

        in.close();
    }
}</code></pre></div>

<h2 id="toc_15">3. [8393번] 합</h2>

<h3 id="toc_16">문제</h3>

<div><pre><code class="language-none">n이 주어졌을 때, 1부터 n까지 합을 구하는 프로그램을 작성하시오.</code></pre></div>

<h3 id="toc_17">입력</h3>

<div><pre><code class="language-none">첫째 줄에 n (1 ≤ n ≤ 10,000)이 주어진다.</code></pre></div>

<h3 id="toc_18">출력</h3>

<div><pre><code class="language-none">1부터 n까지 합을 출력한다.</code></pre></div>

<h3 id="toc_19">예제 입력 1</h3>

<p><code>3</code></p>

<h3 id="toc_20">예제 출력 1</h3>

<p><code>6</code></p>

<h3 id="toc_21">내 제출 코드</h3>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        int sum = 0;

        for(int i = 0; i &lt; n; i++)
        {
            sum += (i+1);
        }

        System.out.println(sum);
        in.close();
    }
}   </code></pre></div>

<h2 id="toc_22">4. [15552번] 빠른 A + B</h2>

<h3 id="toc_23">문제</h3>

<div><pre><code class="language-none">본격적으로 for문 문제를 풀기 전에 주의해야 할 점이 있다. 입출력 방식이 느리면 여러 줄을 입력받거나 출력할 때 시간초과가 날 수 있다는 점이다.

C++을 사용하고 있고 cin/cout을 사용하고자 한다면, cin.tie(NULL)과 sync_with_stdio(false)를 둘 다 적용해 주고, endl 대신 개행문자(\n)를 쓰자. 단, 이렇게 하면 더 이상 scanf/printf/puts/getchar/putchar 등 C의 입출력 방식을 사용하면 안 된다.

Java를 사용하고 있다면, Scanner와 System.out.println 대신 BufferedReader와 BufferedWriter를 사용할 수 있다. BufferedWriter.flush는 맨 마지막에 한 번만 하면 된다.

Python을 사용하고 있다면, input 대신 sys.stdin.readline을 사용할 수 있다. 단, 이때는 맨 끝의 개행문자까지 같이 입력받기 때문에 문자열을 저장하고 싶을 경우 .rstrip()을 추가로 해 주는 것이 좋다.

또한 입력과 출력 스트림은 별개이므로, 테스트케이스를 전부 입력받아서 저장한 뒤 전부 출력할 필요는 없다. 테스트케이스를 하나 받은 뒤 하나 출력해도 된다.</code></pre></div>

<h3 id="toc_24">입력</h3>

<div><pre><code class="language-none">첫 줄에 테스트케이스의 개수 T가 주어진다. T는 최대 1,000,000이다. 다음 T줄에는 각각 두 정수 A와 B가 주어진다. A와 B는 1 이상, 1,000 이하이다.</code></pre></div>

<h3 id="toc_25">출력</h3>

<div><pre><code class="language-none">각 테스트케이스마다 A+B를 한 줄에 하나씩 순서대로 출력한다.</code></pre></div>

<h3 id="toc_26">예제 입력 1</h3>

<div><pre><code class="language-none">5
1 1
12 34
5 500
40 60
1000 1000</code></pre></div>

<h3 id="toc_27">예제 출력 1</h3>

<div><pre><code class="language-none">2
46
505
100
2000</code></pre></div>

<h3 id="toc_28">내 제출 코드</h3>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.StringTokenizer;

public class Main {

    public static void main(String[] args) throws IOException {

        //BufferedReader와 BufferedWriter 선언 
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        //String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
        int T = Integer.parseInt(br.readLine());

        StringTokenizer st;

        for (int i = 0; i &lt; T; i++) {
            //테스트 케이스에서 주어지는 두 정수는 문자열 분리를 위해 매 반복마다 StringTokenizer 생성과 동시에 문자를 입력받는다.
            //public StringTokenizer(String str, String delim) : 특정 delim으로 문자열을 분리한다.
            st = new StringTokenizer(br.readLine(),&quot; &quot;); //한 줄씩 읽어와서(readline), 공백으로 문자열 분리(&quot;&quot;) 
            bw.write((Integer.parseInt(st.nextToken()) + Integer.parseInt(st.nextToken()))+ &quot;\n&quot;);
        }
        br.close();

        bw.flush();
        bw.close();

    }
}   </code></pre></div>

<h2 id="toc_29">5. [2741번] N 찍기</h2>

<h3 id="toc_30">문제</h3>

<div><pre><code class="language-none">자연수 N이 주어졌을 때, 1부터 N까지 한 줄에 하나씩 출력하는 프로그램을 작성하시오.</code></pre></div>

<h3 id="toc_31">입력</h3>

<div><pre><code class="language-none">첫째 줄에 100,000보다 작거나 같은 자연수 N이 주어진다.</code></pre></div>

<h3 id="toc_32">출력</h3>

<div><pre><code class="language-none">첫째 줄부터 N번째 줄 까지 차례대로 출력한다.</code></pre></div>

<h3 id="toc_33">예제 입력 1</h3>

<div><pre><code class="language-none">5</code></pre></div>

<h3 id="toc_34">예제 출력 1</h3>

<div><pre><code class="language-none">1
2
3
4
5</code></pre></div>

<h3 id="toc_35">내 제출 코드</h3>

<ol>
<li><p>&quot;<strong>BufferedReader &amp; BufferedWriter 사용</strong>&quot;  -&gt; 더 efficient</p>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;

public class Main {

    public static void main(String[] args) throws IOException {

        //BufferedReader와 BufferedWriter 선언 
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        //String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
        int N = Integer.parseInt(br.readLine());

        for (int i = 1; i &lt;= N; i++) {
            bw.write(i + &quot;\n&quot;);
        }
        br.close();

        bw.flush();
        bw.close();

    }
}</code></pre></div></li>
<li><p>&quot;<strong>Scanner 사용</strong>&quot;</p>

<div><pre><code class="language-none">import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {

            Scanner in = new Scanner(System.in);
            int N = in.nextInt();

            for(int i = 1; i &lt;=N; i++)
            {
                System.out.println(i);
                //System.out.printf(&quot;%d\n&quot;,i);도 가능!
            }

            in.close();
        }
    }</code></pre></div></li>
</ol>

<ul>
<li>## 6. [2742번] 기찍 N</li>
</ul>

<h3 id="toc_36">문제</h3>

<div><pre><code class="language-none">자연수 N이 주어졌을 때, N부터 1까지 한 줄에 하나씩 출력하는 프로그램을 작성하시오.</code></pre></div>

<h3 id="toc_37">입력</h3>

<div><pre><code class="language-none">첫째 줄에 100,000보다 작거나 같은 자연수 N이 주어진다.</code></pre></div>

<h3 id="toc_38">출력</h3>

<div><pre><code class="language-none">첫째 줄부터 N번째 줄 까지 차례대로 출력한다.</code></pre></div>

<h3 id="toc_39">예제 입력 1</h3>

<div><pre><code class="language-none">5</code></pre></div>

<h3 id="toc_40">예제 출력 1</h3>

<div><pre><code class="language-none">5
4
3
2
1</code></pre></div>

<h3 id="toc_41">내 제출 코드</h3>

<ol>
<li><p>&quot;<strong>BufferedReader &amp; BufferedWriter 사용</strong>&quot;  -&gt; 더 efficient</p>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;

public class Main {

    public static void main(String[] args) throws IOException {

        //BufferedReader와 BufferedWriter 선언 
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        //String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
        int N = Integer.parseInt(br.readLine());

        for (int i = N; i &gt;= 1; i--) {
            bw.write(i + &quot;\n&quot;);
        }
        br.close();

        bw.flush();
        bw.close();

    }
}</code></pre></div></li>
<li><p>&quot;<strong>Scanner 사용</strong>&quot;</p>

<div><pre><code class="language-none">import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {

            Scanner in = new Scanner(System.in);
            int N = in.nextInt();

            for(int i = N; i &gt;= 1; i--)
            {
                System.out.println(i);
                //System.out.printf(&quot;%d\n&quot;,i);도 가능!
            }

            in.close();
        }
    }</code></pre></div></li>
</ol>

<h2 id="toc_42">7. [11021번] A+B - 7</h2>

<h3 id="toc_43">문제</h3>

<div><pre><code class="language-none">두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.</code></pre></div>

<h3 id="toc_44">입력</h3>

<div><pre><code class="language-none">첫째 줄에 테스트 케이스의 개수 T가 주어진다.

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 &lt; A, B &lt; 10)</code></pre></div>

<h3 id="toc_45">출력</h3>

<div><pre><code class="language-none">각 테스트 케이스마다 &quot;Case #x: &quot;를 출력한 다음, A+B를 출력한다. 테스트 케이스 번호는 1부터 시작한다.</code></pre></div>

<h3 id="toc_46">예제 입력 1</h3>

<div><pre><code class="language-none">5
1 1
2 3
3 4
9 8
5 2</code></pre></div>

<h3 id="toc_47">예제 출력 1</h3>

<div><pre><code class="language-none">Case #1: 2
Case #2: 5
Case #3: 7
Case #4: 17
Case #5: 7</code></pre></div>

<h3 id="toc_48">내 제출 코드</h3>

<ol>
<li><p>&quot;<strong>BufferedReader &amp; BufferedWriter 사용</strong>&quot;  -&gt; 더 efficient</p>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.StringTokenizer;
import java.io.IOException;

public class Main {
    public static void main(String args[]) throws IOException {

        BufferedReader br= new BufferedReader(new InputStreamReader(System.in));

        int T = Integer.parseInt(br.readLine());
        int A;
        int B;

        StringTokenizer st;
        for (int i = 1; i &lt;= T; i++) {
            st = new StringTokenizer(br.readLine(),&quot; &quot;);
            A = Integer.parseInt(st.nextToken());
            B = Integer.parseInt(st.nextToken());
            System.out.println(&quot;Case #&quot; + i + &quot;: &quot; + A + &quot; + &quot; + B + &quot; = &quot; + (A+B));
        }
        br.close();
    }

}   </code></pre></div></li>
<li><p>&quot;<strong>Scanner 사용</strong>&quot;</p>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int T = in.nextInt();

        for(int i = 1; i &lt;= T; i++)
        {
            int A = in.nextInt();
            int B = in.nextInt();
            System.out.println(&quot;Case #&quot; + i +&quot;: &quot; + A + &quot; + &quot; + B + &quot; = &quot; + (A+B));
            //System.out.printf(&quot;Case #%d: %d + %d = %d\n&quot;,i, A, B, (A+B));
        }

        in.close();
    }
}</code></pre></div></li>
</ol>

<h2 id="toc_49">8. [11022번] A+B - 8</h2>

<h3 id="toc_50">문제</h3>

<div><pre><code class="language-none">두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.</code></pre></div>

<h3 id="toc_51">입력</h3>

<div><pre><code class="language-none">첫째 줄에 테스트 케이스의 개수 T가 주어진다.

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 &lt; A, B &lt; 10)</code></pre></div>

<h3 id="toc_52">출력</h3>

<div><pre><code class="language-none">각 테스트 케이스마다 &quot;Case #x: A + B = C&quot; 형식으로 출력한다. x는 테스트 케이스 번호이고 1부터 시작하며, C는 A+B이다.</code></pre></div>

<h3 id="toc_53">예제 입력 1</h3>

<div><pre><code class="language-none">5
1 1
2 3
3 4
9 8
5 2</code></pre></div>

<h3 id="toc_54">예제 출력 1</h3>

<div><pre><code class="language-none">Case #1: 1 + 1 = 2
Case #2: 2 + 3 = 5
Case #3: 3 + 4 = 7
Case #4: 9 + 8 = 17
Case #5: 5 + 2 = 7</code></pre></div>

<h3 id="toc_55">내 제출 코드</h3>

<ol>
<li><p>&quot;<strong>BufferedReader &amp; BufferedWriter 사용</strong>&quot;  -&gt; 더 efficient</p>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.StringTokenizer;

public class Main {

    public static void main(String[] args) throws IOException {

        //BufferedReader와 BufferedWriter 선언 
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        //String값을 Integer.parselnt를 통해 int형으로 바꾸어 준다. 
        int T = Integer.parseInt(br.readLine());

        StringTokenizer st;

        for (int i = 1; i &lt;= T; i++) {
            //테스트 케이스에서 주어지는 두 정수는 문자열 분리를 위해 매 반복마다 StringTokenizer 생성과 동시에 문자를 입력받는다.
            //public StringTokenizer(String str, String delim) : 특정 delim으로 문자열을 분리한다.
            st = new StringTokenizer(br.readLine(),&quot; &quot;); //한 줄씩 읽어와서(readline), 공백으로 문자열 분리(&quot;&quot;) 
            int A = Integer.parseInt(st.nextToken());
            int B = Integer.parseInt(st.nextToken());
            bw.write(&quot;Case #&quot; + i + &quot;: &quot; + A + &quot; + &quot; + B + &quot; = &quot; + (A+B) + &quot;\n&quot;);
        }
        br.close();

        bw.flush();
        bw.close();

    }
}   </code></pre></div></li>
<li><p>&quot;<strong>Scanner 사용</strong>&quot;</p>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int T = in.nextInt();

        for(int i = 1; i &lt;= 5; i++)
        {
            int A = in.nextInt();
            int B = in.nextInt();
            System.out.println(&quot;Case #&quot; + i +&quot;: &quot; + (A+B));
            //System.out.printf(&quot;Case #%d: %d\n&quot;,i, (A+B));도 가능!
        }

        in.close();
    }
}</code></pre></div></li>
</ol>

<h2 id="toc_56">9. [2438번] 별 찍기 - 1</h2>

<h3 id="toc_57">문제</h3>

<div><pre><code class="language-none">첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제 </code></pre></div>

<h3 id="toc_58">입력</h3>

<div><pre><code class="language-none">첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.</code></pre></div>

<h3 id="toc_59">출력</h3>

<div><pre><code class="language-none">첫째 줄부터 N번째 줄까지 차례대로 별을 출력한다.</code></pre></div>

<h3 id="toc_60">예제 입력 1</h3>

<div><pre><code class="language-none">5</code></pre></div>

<h3 id="toc_61">예제 출력 1</h3>

<div><pre><code class="language-none">*
**
***
****
*****</code></pre></div>

<h3 id="toc_62">내 제출 코드</h3>

<ol>
<li><p>&quot;<strong>BufferedReader &amp; BufferedWriter 사용</strong>&quot;  -&gt; 더 efficient</p>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.io.IOException;

public class Main {
    public static void main(String args[]) throws IOException {

        BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        int N = Integer.parseInt(br.readLine());

        for (int i = 1; i &lt;= N; i++) {
            for(int j = 1; j&lt;=i; j++) {
                bw.write(&quot;*&quot;);
            }
            bw.write(&quot;\n&quot;);
        }

        br.close();

        bw.flush();
        bw.close();
    }

}</code></pre></div></li>
<li><p>&quot;<strong>Scanner 사용</strong>&quot;</p>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int N = in.nextInt();

        for(int i = 1; i &lt;= N; i++)
        {
            for(int j =1; j&lt;=i; j++)
            {
                System.out.printf(&quot;*&quot;);
            }
            System.out.printf(&quot;\n&quot;);
        }

        in.close();
    }
}</code></pre></div></li>
</ol>

<h2 id="toc_63">10. [2439번] 별 찍기 - 2</h2>

<h3 id="toc_64">문제</h3>

<div><pre><code class="language-none">첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제

하지만, 오른쪽을 기준으로 정렬한 별(예제 참고)을 출력하시오. </code></pre></div>

<h3 id="toc_65">입력</h3>

<div><pre><code class="language-none">첫째 줄에 N(1 ≤ N ≤ 100)이 주어진다.</code></pre></div>

<h3 id="toc_66">출력</h3>

<div><pre><code class="language-none">첫째 줄부터 N번째 줄까지 차례대로 별을 출력한다.</code></pre></div>

<h3 id="toc_67">예제 입력 1</h3>

<div><pre><code class="language-none">5</code></pre></div>

<h3 id="toc_68">예제 출력 1</h3>

<div><pre><code class="language-none">    *
   **
  ***
 ****
*****</code></pre></div>

<h3 id="toc_69">내 제출 코드</h3>

<ol>
<li><p>&quot;<strong>BufferedReader &amp; BufferedWriter 사용</strong>&quot;  -&gt; 더 efficient</p>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.io.IOException;

public class Main {
    public static void main(String args[]) throws IOException {

        BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

        int N = Integer.parseInt(br.readLine());

        for (int i = 1; i &lt;= N; i++) {
            for(int j = 1; j&lt;=N-i; j++) {
                bw.write(&quot; &quot;);
            }
            for(int j = 1; j&lt;=i; j++) {
                bw.write(&quot;*&quot;);
            }
            bw.write(&quot;\n&quot;);
        }

        br.close();

        bw.flush();
        bw.close();
    }

}</code></pre></div></li>
<li><p>&quot;<strong>Scanner 사용</strong>&quot;</p>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner in = new Scanner(System.in);
        int N = in.nextInt();

        for(int i = 1; i &lt;= N; i++)
        {
            for(int j =1; j&lt;=N-i; j++)
            {
                System.out.printf(&quot; &quot;);
            }
            for(int j = 1; j&lt;=i; j++) {
                System.out.printf(&quot;*&quot;);
            }
            System.out.printf(&quot;\n&quot;);
        }

        in.close();
    }
}</code></pre></div></li>
</ol>

<h2 id="toc_70">11. [10871번] X보다 작은 수</h2>

<h3 id="toc_71">문제</h3>

<div><pre><code class="language-none">정수 N개로 이루어진 수열 A와 정수 X가 주어진다. 이때, A에서 X보다 작은 수를 모두 출력하는 프로그램을 작성하시오.</code></pre></div>

<h3 id="toc_72">입력</h3>

<div><pre><code class="language-none">첫째 줄에 N과 X가 주어진다. (1 ≤ N, X ≤ 10,000)

둘째 줄에 수열 A를 이루는 정수 N개가 주어진다. 주어지는 정수는 모두 1보다 크거나 같고, 10,000보다 작거나 같은 정수이다.</code></pre></div>

<h3 id="toc_73">출력</h3>

<div><pre><code class="language-none">X보다 작은 수를 입력받은 순서대로 공백으로 구분해 출력한다. X보다 작은 수는 적어도 하나 존재한다.</code></pre></div>

<h3 id="toc_74">예제 입력 1</h3>

<div><pre><code class="language-none">10 5
1 10 4 9 2 3 8 5 7 6</code></pre></div>

<h3 id="toc_75">예제 출력 1</h3>

<div><pre><code class="language-none">1 4 2 3</code></pre></div>

<h3 id="toc_76">내 제출 코드</h3>

<ol>
<li><p>&quot;<strong>BufferedReader &amp; BufferedWriter 사용</strong>&quot;  -&gt; 더 efficient</p>

<div><pre><code class="language-none">import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.StringTokenizer;

public class Main {

    public static void main(String[] args) throws IOException {

        //BufferedReader 선언 
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        StringTokenizer st = new StringTokenizer(br.readLine(), &quot; &quot;);

        int N = Integer.parseInt(st.nextToken());
        int X = Integer.parseInt(st.nextToken());

        StringBuilder sb = new StringBuilder();

        st = new StringTokenizer(br.readLine(),&quot; &quot;);

        for (int i = 0; i &lt; N; i++) {
            int value = Integer.parseInt(st.nextToken());

            if (value &lt; X)
                sb.append(value).append(&#39; &#39;);
        }
        System.out.println(sb);

    }
}   </code></pre></div></li>
<li><p>&quot;<strong>Scanner 사용</strong>&quot;</p></li>
</ol>

<p>[1] 따로 입력값들을 저장하지 않고, 바로바로 값을 입력받고 바로바로 체크해서 출력하는 방법</p>

<div><pre><code class="language-none">    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {

            Scanner in = new Scanner(System.in);
            int N = in.nextInt();
            int X = in.nextInt();

            for(int i = 1; i &lt;= N; i++)
            {
                int input = in.nextInt();
                if( input &lt; X )
                    System.out.printf(&quot;%d &quot;,input);
            }

            in.close();
        }
    }</code></pre></div>

<p>[2] 입력받음과 동시에 if 문으로 검사해서 주어진 수 보다 작은 경우 &quot;<strong>StringBuilder</strong>&quot; 에 저장해주는 방법</p>

<div><pre><code class="language-none">import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int N = in.nextInt();
        int X = in.nextInt();

        StringBuilder sb = new StringBuilder();

        for(int i = 0 ; i &lt; N ; i++) {

            int value = in.nextInt();
            if(value &lt; X) {
                sb.append(value+&quot; &quot;);
            }
        }
        System.out.println(sb); 
    }
}</code></pre></div>
