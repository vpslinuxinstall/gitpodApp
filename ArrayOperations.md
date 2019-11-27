# Array operations             

## Lecture      

<iframe src="assets/ArrayOperations.webm" width="560" height="315" frameborder="0" allowfullscreen></iframe>      

## Operations on Arrays      

<div class="markdown-zone" data-open-new-tab="">
            
<h2 id="python">Python</h2>

<h3 id="accessing-elements">Accessing Elements</h3>

<p>Use the index operator on a list to access values using an index. Note that index values start at 0.</p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">]</span>
</span><span id="line-2"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span>
</span><span id="line-3"><span class="mi">3</span>
</span></pre></div>

<p>Using an index that is out of bounds of the current range of values results in a runtime error.</p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="p">[</span><span class="mi">12</span><span class="p">]</span>
</span><span id="line-2"><span class="n">Traceback</span> <span class="p">(</span><span class="n">most</span> <span class="n">recent</span> <span class="n">call</span> <span class="n">last</span><span class="p">):</span>
</span><span id="line-3">  <span class="n">File</span> <span class="s2">"&lt;stdin&gt;"</span><span class="p">,</span> <span class="n">line</span> <span class="mi">1</span><span class="p">,</span> <span class="ow">in</span> <span class="o">&lt;</span><span class="n">module</span><span class="o">&gt;</span>
</span><span id="line-4"><span class="ne">IndexError</span><span class="p">:</span> <span class="nb">list</span> <span class="n">index</span> <span class="n">out</span> <span class="n">of</span> <span class="nb">range</span>
</span></pre></div>

<h3 id="list-length">List Length</h3>

<p>To determine the number of items in a list, use the <code>len</code> function. </p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="nb">len</span><span class="p">(</span><span class="n">numbers</span><span class="p">)</span>
</span><span id="line-2"><span class="mi">6</span>
</span></pre></div>

<p><code>len</code> is often used to determine the range of valid index values in a list. To avoid runtime errors it is good practice to iterate over a list with a range defined by the result of calling <code>len</code> instead of a hard coded constant.</p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">numbers</span><span class="p">)):</span>
</span><span id="line-2"><span class="o">...</span>     <span class="k">print</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
</span><span id="line-3"><span class="o">...</span>
</span><span id="line-4"><span class="mi">1</span>
</span><span id="line-5"><span class="mi">2</span>
</span><span id="line-6"><span class="mi">3</span>
</span><span id="line-7"><span class="mi">4</span>
</span><span id="line-8"><span class="mi">5</span>
</span><span id="line-9"><span class="mi">6</span>
</span></pre></div>

<h3 id="list-operations">List Operations</h3>

<p>To add to a list, use the <code>append(x)</code> method</p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mi">7</span><span class="p">)</span>
</span></pre></div>

<p>To add (or concatenate) one list to another, use <code>extend(iterable)</code></p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="o">.</span><span class="n">extend</span><span class="p">([</span><span class="mi">8</span><span class="p">,</span> <span class="mi">9</span><span class="p">,</span> <span class="mi">10</span><span class="p">])</span>
</span></pre></div>

<p>To insert an item into a list at a given position. Here the value 11 is inserted at index position 10.</p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="o">.</span><span class="n">insert</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">11</span><span class="p">)</span>
</span></pre></div>

<p>Use the <code>remove(x)</code> method to remove an item from a list. <code>remove()</code> takes a value as an argument and removes the first element in the list that matches the argument.</p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="o">.</span><span class="n">remove</span><span class="p">(</span><span class="mi">11</span><span class="p">)</span>
</span></pre></div>

<p>Searching for the position of an element in a list is possible using the <code>index(x)</code></p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="mi">4</span><span class="p">)</span>
</span><span id="line-2"><span class="mi">3</span>
</span></pre></div>

<h3 id="list-membership">List Membership</h3>

<p>Use the <code>in</code> and <code>not in</code> operators to test for membership in a list. </p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="k">if</span> <span class="mi">5</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span> <span class="k">print</span><span class="p">(</span><span class="bp">True</span><span class="p">)</span>
</span><span id="line-2"><span class="bp">True</span>
</span><span id="line-3"><span class="o">&gt;&gt;&gt;</span> <span class="k">if</span> <span class="mi">30</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span> <span class="k">print</span><span class="p">(</span><span class="bp">True</span><span class="p">)</span>
</span><span id="line-4"><span class="bp">True</span>
</span></pre></div>

<p>Python lists are mutable which means any element can be updated using the index operator along with an index position.</p>

<div class="highlight highlight-python"><pre><span></span><span id="line-1"><span class="o">&gt;&gt;&gt;</span> <span class="n">numbers</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="mi">22</span> <span class="c1"># Updates first element in list to 22</span>
</span></pre></div>

<p><strong>Additional Resources:</strong></p>

<ul>
<li><a href="http://openbookproject.net/thinkcs/python/english3e/lists.html" target="_blank">Lists</a></li>
<li><a href="https://docs.python.org/3/tutorial/datastructures.html" target="_blank">List Operations</a></li>
</ul>

<hr>

<h2 id="swift">Swift</h2>

<h3 id="accessing-elements">Accessing Elements</h3>

<p>Accessing elements individually is generally done using subscript notation with index values starting at 0.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">numbers</span><span class="p">:</span> <span class="p">[</span><span class="nb">Int</span><span class="p">]</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">]</span>
</span><span id="line-2"><span class="kd">let</span> <span class="nv">firstValue</span> <span class="p">=</span> <span class="n">numbers</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
</span></pre></div>

<p>You can subscript an array with any integer starting from 0 up to, but not including, the count of the array. Unlike languages like Python you cannot use a negative number or an index equal to or greater than <code>count</code>. This triggers a runtime error.</p>

<p>In addition to subscripting, there are several methods defined on the type that offer a degree of safety when accessing values. Use the <code>first</code> and <code>last</code> properties to get the first and last elements of an array.</p>

<p>Both these properties return optional values so you can guard against them instead of hitting a runtime error.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="k">if</span> <span class="kd">let</span> <span class="nv">firstElement</span> <span class="p">=</span> <span class="n">numbers</span><span class="p">.</span><span class="bp">first</span><span class="p">,</span> <span class="kd">let</span> <span class="nv">lastElement</span> <span class="p">=</span> <span class="n">numbers</span><span class="p">.</span><span class="bp">last</span> <span class="p">{</span>
</span><span id="line-2">    <span class="bp">print</span><span class="p">(</span><span class="n">firstElement</span><span class="p">,</span> <span class="n">lastElement</span><span class="p">,</span> <span class="n">separator</span><span class="p">:</span> <span class="s">", "</span><span class="p">)</span>
</span><span id="line-3"><span class="p">}</span>
</span><span id="line-4">
</span><span id="line-5"><span class="n">To</span> <span class="n">iterate</span> <span class="n">over</span> <span class="n">a</span> <span class="n">the</span> <span class="n">entire</span> <span class="n">array</span> <span class="n">use</span> <span class="n">a</span> <span class="p">`</span><span class="k">for</span><span class="o">-</span><span class="k">in</span><span class="p">`</span> <span class="n">loop</span><span class="p">.</span>
</span><span id="line-6">
</span><span id="line-7"><span class="p">```</span><span class="n">swift</span>
</span><span id="line-8"><span class="k">for</span> <span class="n">number</span> <span class="k">in</span> <span class="n">numbers</span> <span class="p">{</span>
</span><span id="line-9">    <span class="bp">print</span><span class="p">(</span><span class="n">number</span><span class="p">)</span>
</span><span id="line-10"><span class="p">}</span>
</span></pre></div>

<p>You can also call <code>enumerated()</code> on an array to return a sequence of pairs <code>(n, x)</code> where <code>n</code> representes the index value and <code>x</code> represents the element.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="k">for</span> <span class="p">(</span><span class="n">index</span><span class="p">,</span> <span class="n">element</span><span class="p">)</span> <span class="k">in</span> <span class="n">numbers</span><span class="p">.</span><span class="n">enumerated</span><span class="p">()</span> <span class="p">{</span>
</span><span id="line-2">    <span class="bp">print</span><span class="p">(</span><span class="s">"Element </span><span class="si">\(</span><span class="n">element</span><span class="si">)</span><span class="s"> is at index position </span><span class="si">\(</span><span class="n">index</span><span class="si">)</span><span class="s">"</span><span class="p">)</span>
</span><span id="line-3"><span class="p">}</span>
</span></pre></div>

<h3 id="adding-and-removing-elements">Adding and Removing Elements</h3>

<p>Arrays can only be modified if they are assigned to a variable and not a constant. </p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">numbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>
</span><span id="line-2"><span class="n">numbers</span><span class="p">.</span><span class="n">append</span><span class="p">(</span><span class="mi">4</span><span class="p">)</span> <span class="c1">// Cannot use mutating member on immutable value: 'numbers' is a 'let' constant</span>
</span></pre></div>

<p>Use the <code>append(_:)</code> method to add values to the end of a variable array</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">var</span> <span class="nv">numbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">]</span>
</span><span id="line-2"><span class="n">numbers</span><span class="p">.</span><span class="n">append</span><span class="p">(</span><span class="mi">6</span><span class="p">)</span>
</span></pre></div>

<p>When appending more than one value, you have several options. You can concatenate one array to another <em>provided they are of the same type</em>.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">numbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">]</span>
</span><span id="line-2"><span class="n">numbers</span> <span class="o">+</span> <span class="p">[</span><span class="mi">6</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">]</span>
</span></pre></div>

<p>Notice that the concatenation operation is carried out an array assigned to a constant. This is because the concatenation operation does not mutate the original array and returns a new array containing values from both. </p>

<p>To mutate the array and add multiple elements at the same time by passing another array or a sequence use the <code>append(contentsOf:)</code> method.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">var</span> <span class="nv">numbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">]</span>
</span><span id="line-2"><span class="n">numbers</span><span class="p">.</span><span class="n">append</span><span class="p">(</span><span class="n">contentsOf</span><span class="p">:</span> <span class="p">[</span><span class="mi">6</span><span class="p">,</span> <span class="mi">7</span> <span class="p">,</span><span class="mi">8</span><span class="p">])</span>
</span></pre></div>

<p>All of these operations add elements to the end of an array. To insert an element in the middle of an array use the <code>insert(_:at:)</code> method for single elements or the <code>insert(contentsOf:at:)</code> method for multiple elements. </p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">var</span> <span class="nv">numbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">]</span>
</span><span id="line-2"><span class="n">numbers</span><span class="p">.</span><span class="bp">insert</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="n">at</span><span class="p">:</span> <span class="mi">2</span><span class="p">)</span>
</span><span id="line-3"><span class="n">numbers</span><span class="p">.</span><span class="bp">insert</span><span class="p">(</span><span class="n">contentsOf</span><span class="p">:</span> <span class="p">[</span><span class="mi">18</span><span class="p">,</span> <span class="mi">22</span><span class="p">,</span> <span class="mi">35</span><span class="p">],</span> <span class="n">at</span><span class="p">:</span> <span class="mi">4</span><span class="p">)</span>
</span></pre></div>

<p>To remove elements from an array there are three options. To remove a single element at an index, use the <code>remove(at:)</code> method. </p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="n">numbers</span><span class="p">.</span><span class="n">remove</span><span class="p">(</span><span class="n">at</span><span class="p">:</span> <span class="mi">2</span><span class="p">)</span>
</span></pre></div>

<p>To remove multiple elements use the <code>removeSubrange(_:)</code> method along with a range, either the half-open range operator <code>(..&lt;)</code> or the closed range operator <code>(...)</code>.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="n">numbers</span><span class="p">.</span><span class="n">removeSubrange</span><span class="p">(</span><span class="mf">3.</span><span class="p">..</span><span class="mi">6</span><span class="p">)</span>
</span><span id="line-2"><span class="n">numbers</span><span class="p">.</span><span class="n">removeSubrange</span><span class="p">(</span><span class="mf">3.</span><span class="p">.&lt;</span><span class="mi">7</span><span class="p">)</span>
</span></pre></div>

<p>Finally, you can use the convenience methods <code>removeFirst()</code> and <code>removeLast()</code> to remove the first and last elements in the array. </p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="n">numbers</span><span class="p">.</span><span class="n">removeFirst</span><span class="p">()</span> <span class="c1">// 1</span>
</span><span id="line-2"><span class="n">numbers</span><span class="p">.</span><span class="bp">removeLast</span><span class="p">()</span>
</span></pre></div>

<h3 id="querying-an-array">Querying An Array</h3>

<p>To determine the number of elements in the array use the <code>count</code> property</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">numbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>
</span><span id="line-2"><span class="n">numbers</span><span class="p">.</span><span class="bp">count</span> <span class="c1">// 3</span>
</span></pre></div>

<p>To determine whether an array is empty use the <code>isEmpty</code> property</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="k">if</span> <span class="n">numbers</span><span class="p">.</span><span class="bp">isEmpty</span> <span class="p">{</span>
</span><span id="line-2">    <span class="c1">// do something</span>
</span><span id="line-3"><span class="p">}</span>
</span></pre></div>

<h3 id="array-membership">Array Membership</h3>

<p>To check whether an element exists in an array, use the <code>contains(_:)</code> method.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="n">numbers</span><span class="p">.</span><span class="bp">contains</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>
</span></pre></div>

<p>You can also use <code>contains(where:)</code> to search for an element that satisfies a predicate.</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="n">numbers</span><span class="p">.</span><span class="bp">contains</span><span class="p">(</span><span class="k">where</span><span class="p">:</span> <span class="p">{</span> <span class="nv">$0</span> <span class="o">%</span> <span class="mi">2</span> <span class="p">==</span> <span class="mi">0</span> <span class="p">})</span>
</span></pre></div>

<p>To find the first instance of an element and return its index position use <code>firstIndex(of:)</code>. </p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="n">numbers</span><span class="p">.</span><span class="n">firstIndex</span><span class="p">(</span><span class="n">of</span><span class="p">:</span> <span class="mi">10</span><span class="p">)</span>
</span></pre></div>

<p>Similarly use <code>lastIndex(of:)</code> to return the last index where the specified value appears in the array.</p>

<h3 id="creating-array-slices">Creating Array Slices</h3>

<p>Often times you will want to extract or query only a portion of an array and you can do this using array slices. Array slices are created when a range is used with a subscript. </p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">someNumbers</span> <span class="p">=</span> <span class="n">numbers</span><span class="p">[</span><span class="mf">2.</span><span class="p">..</span><span class="mi">6</span><span class="p">]</span>
</span></pre></div>

<p>There are couple interesting points to array slices you should be aware of if you're coming from another language:</p>

<ul>
<li>Slicing an array returns a different type - <code>ArraySlice</code>. <code>someNumber</code> in the code snippet above is of type <code>ArraySlice&lt;Int&gt;</code>.</li>
<li>
<code>ArraySlice</code>, like <code>Array</code> is a generic type that infers the type of <code>Element</code> from the array it was dervied from. It cannot be used where the type <code>Array</code> is expected.</li>
<li>In addition, array slices maintain index values of the parent array. </li>
</ul>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">numbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">18</span><span class="p">,</span> <span class="mi">22</span><span class="p">,</span> <span class="mi">35</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">]</span>
</span><span id="line-2"><span class="kd">let</span> <span class="nv">someNumbers</span> <span class="p">=</span> <span class="n">numbers</span><span class="p">[</span><span class="mf">2.</span><span class="p">..</span><span class="mi">6</span><span class="p">]</span> <span class="c1">// [10, 3, 18, 22, 35]</span>
</span><span id="line-3"><span class="n">someNumbers</span><span class="p">.</span><span class="n">firstIndex</span><span class="p">(</span><span class="n">of</span><span class="p">:</span> <span class="mi">18</span><span class="p">)</span>
</span></pre></div>

<p>In the code snippet above while it seems like <code>firstIndex(of:)</code> should return the value 2, the value returned is actually 4. This is becase someNumbers maintains the indices of its parent array. This is because array slices are acttually just <em>views</em> into an array.  </p>









```python      
new_list = [1, 2, 3]
result = new_list[0]

if 1 in new_list: print(True)
  
for n in new_list:
  if n == 1:
    print(True)
    
    break

# Adding to a list
new_list.append(4)
new_list.extend([5, 6, 7])

# Inserting in a list
new_list.insert(0, 10)

# Deleting specific value in a list
new_list.remove(4)      

```        





