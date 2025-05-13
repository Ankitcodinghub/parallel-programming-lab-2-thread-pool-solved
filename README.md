# parallel-programming-lab-2-thread-pool-solved
**TO GET THIS SOLUTION VISIT:** [Parallel_programming Lab 2-Thread pool Solved](https://www.ankitcodinghub.com/product/parallel_programming-lab-2-thread-pool-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92755&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Parallel_programming Lab 2-Thread pool Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Part II : Thread pool

</div>
</div>
<div class="layoutArea">
<div class="column">
1.

</div>
<div class="column">
Design a thread pool class with following features:

A. Allow users to send jobs into the pool

B. Allow any kind of callable objects as jobs

C. Maintain a job queue to store unfinished jobs

</div>
</div>
<div class="layoutArea">
<div class="column">
2.

3. 4.

</div>
<div class="column">
Write one function (named print_1), which can generate a random integer number and then print out ‘1’ if the number is an odd number otherwise ‘0’. Note that cout is also a shared resource.

Write a print_2 functor, which simply prints “2” on the screen. Use conditional variable to ensure that print_2 functor can only be executed when there is no more print_1 job to be executed.

In main, first send 496 functions and then 4 functors into the pool.

</div>
</div>
<div class="layoutArea">
<div class="column">
D. E.

F.

</div>
<div class="column">
i. Hint: element type: std::function/std::bind or package_task

Have 5 threads always waiting for new jobs. Each thread will keep a record of total running time throughout the lifespan of the thread.

Threads are terminated(joined) only when the thread pool is

destructed. The total running time of each thread will be shown on the screen upon destruction along with the std::thread::id.

Use condition variable and mutex to notify threads to do works

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
#include&lt;queue&gt; #include&lt;functional&gt; #include&lt;iostream&gt; Void add()

</div>
</div>
<div class="layoutArea">
<div class="column">
{ }

struct ADD {

{

int main(void) {

</div>
</div>
<div class="layoutArea">
<div class="column">
} };

</div>
<div class="column">
std::cerr&lt;&lt;”2”&lt;&lt;std::endl;

</div>
</div>
<div class="layoutArea">
<div class="column">
std::cerr&lt;&lt;“1”&lt;&lt;std::endl;

void operator()()

</div>
</div>
<div class="layoutArea">
<div class="column">
ADD a;

std::queue&lt; std::function&lt;void(void)&gt; &gt; jobs; jobs.push( std::bind(add) );

jobs.push( std::bind( std::bind(a) ) ); jobs.push( std::bind(a) );

while(!jobs.empty() )

{

jobs.front()();

</div>
</div>
<div class="layoutArea">
<div class="column">
jobs.pop(); }

return 0; }

</div>
</div>
</div>
