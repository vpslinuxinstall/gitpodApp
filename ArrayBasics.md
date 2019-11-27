# Array basics     




## Lecture        

<iframe src="assets/Array.webm" width="560" height="315" frameborder="0" allowfullscreen></iframe>     

## Array Characteristics and Storage     

<div class="markdown-zone" data-open-new-tab="">
            

<h2 id="python">Python</h2>

<p>Python defines both an <code>array</code> and a <code>list</code> type and while they look and feel similar to one another they have their own uses. The <code>array.array</code> class in Python is a thin <a href="https://stackoverflow.com/a/889178/1071846" target="_blank">wrapper</a> around a C array and this introduces some limitations. For example, Python arrays are homogeneous and can only hold data of a single kind. The type does take up much less space in memory than Python lists however so in general you would use an array if space was a concern or if you wanted to expose some C functionality. </p>

<p>As mentioned in the course, Python lists are the more frequently used type and the de facto representation of an <em>array like</em> structure. They are a heterogeneous and contiguous data structure. </p>

<hr>

<h2 id="java">Java</h2>

<p>Arrays in Java are represented by the <code>Array</code> class and is a homogeneous container containing a fixed number of values of a single type. Two types of arrays can be created - one containing primitive values like <code>int</code> or <code>char</code> or ones that contain objects by means of references or pointers.  </p>

<p>To declare a variable to refer to an array the type must be specified. </p>

<div class="highlight highlight-java"><pre><span></span><span id="line-1"><span class="c1">// declares an array of integers</span>
</span><span id="line-2"><span class="kt">int</span><span class="o">[]</span> <span class="n">anArray</span><span class="o">;</span>
</span></pre></div>

<p>Declaring an array does not actually create the array, instead it indicates that the variable holds an array of the type that we specify. When an array is created the variable <code>anArray</code> holds a reference to the location in memory where the array is stored. </p>

<p>When arrays of primitive values are created, the values are stored in the array. For objects however, the array contains references to the locations in memory where the objects are stored. </p>

<hr>

<h2 id="javascript">JavaScript</h2>

<p>JavaScript does not have an explicit array data type and arrays are represented by the <code>Array</code> object which is a <em>list like</em> object. <code>Array</code> is an <code>Object</code> type with special constructor and accessor methods. Its prototype has methods to perform traversal and mutation operations.</p>

<p>JavaScript arrays are heterogeneous, meaning the types of elements are not fixed and neither is the size. Unlike the description given in the course video, arrays in JavaScript are <strong>not</strong> contiguous data structures and the data stored in the array can be located in a non-contiguous location. </p>

<p>There are several ways to create an array:</p>

<div class="highlight highlight-js"><pre><span></span><span id="line-1"><span class="kd">var</span> <span class="nx">arr</span> <span class="o">=</span> <span class="k">new</span> <span class="nb">Array</span><span class="p">(</span><span class="mi">1</span><span class="p">);</span>
</span><span id="line-2"><span class="kd">var</span> <span class="nx">arr</span> <span class="o">=</span> <span class="nb">Array</span><span class="p">(</span><span class="mi">1</span><span class="p">);</span>
</span><span id="line-3"><span class="kd">var</span> <span class="nx">arr</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">];</span>
</span></pre></div>

<p>Since arrays are regular JavaScript objects with syntactic sugar there are some nuances to their behavior. Creating a new array does not allocate any memory and the size of an array and its corresponding length are not always the same. </p>

<p>Consider the following snippet:</p>

<div class="highlight highlight-js"><pre><span></span><span id="line-1"><span class="kd">var</span> <span class="nx">values</span> <span class="o">=</span> <span class="p">[];</span>
</span><span id="line-2"><span class="nx">values</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="mi">1</span><span class="p">;</span>
</span><span id="line-3"><span class="nx">values</span><span class="p">[</span><span class="mi">9</span><span class="p">]</span> <span class="o">=</span> <span class="mi">2</span><span class="p">;</span>
</span></pre></div>

<p>Here an array has been created and two values have been inserted at index positions 0 and 9. The length of the array here is actually 10, even though there are only 2 elements in the array. </p>

<p><strong>Additional Resources:</strong></p>

<ul>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array" target="_blank">MDN: Array</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections" target="_blank">MDN: Indexed Collections</a></li>
</ul>

<hr>

<h2 id="swift">Swift</h2>

<p>The <code>Array</code> type in Swift is a generic, homogenous data structure containing values of a single type and is the de facto list data structure. When creating an array the type of the elements can be inferred, making type specification optional. </p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">oddNumbers</span> <span class="p">=</span> <span class="p">[</span><span class="mi">3</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">7</span><span class="p">]</span> <span class="c1">// Type inferred</span>
</span><span id="line-2"><span class="kd">let</span> <span class="nv">evenNumbers</span><span class="p">:</span> <span class="p">[</span><span class="nb">Int</span><span class="p">]</span> <span class="p">=</span> <span class="p">[</span><span class="mi">2</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">6</span><span class="p">]</span> <span class="c1">// Explicit type annotation</span>
</span></pre></div>

<p>In addition, arrays can be created using the literal syntax or by specifying the generic type parameters directly. To create an empty array:</p>

<div class="highlight highlight-swift"><pre><span></span><span id="line-1"><span class="kd">let</span> <span class="nv">vowels</span><span class="p">:</span> <span class="p">[</span><span class="nb">String</span><span class="p">]</span> <span class="p">=</span> <span class="p">[]</span>
</span><span id="line-2"><span class="kd">let</span> <span class="nv">consonants</span> <span class="p">=</span> <span class="nb">Array</span><span class="p">&lt;</span><span class="nb">String</span><span class="p">&gt;()</span>
</span></pre></div>

<p>When creating an empty array using the literal syntax the type must be explicitly specified. </p>

<p>When an array is created a specific amount of memory is allocated to store the values. As the array begins to exceed this reserved capacity, a larger region of memory that is a multiple of the original size is allocated and the values are copied over into the new memory. This exponential growth strategy means that appending an element happens in constant time, averaging the performance of many append operations.</p>

<p>If the desired size of the array is known beforehand, the <code>reserveCapacity(_:)</code> method can be used before appending to the array to avoid intermediate reallocations.</p>

<p>Array storage can be either in contiguous or non-contiguous memory. If the underlying element is a value type then the memory allocated is guaranteed to be contiguous but if the values stored are references types (i.e, classes), then the memory <em>can</em> either be contiguous or an instance of <code>NSArray</code> if the objects stored are <code>@objc</code> types. </p>

<p>Contiguous memory can be guaranteed by using the <code>ContiguousArray</code> type.</p>

<p>Arrays in Swift are value types and implement copy-on-write behavior. Multiple copies of an array share the same storage until one of them is modified. When a copy is modified, the array being modified replaces its (shared) storage with a uniquely owned copy of itself.</p>

<p>When storing value types, the value is stored directly in the array's storage. On the other hand, when reference types are stored, the array stores a pointer to the location in memory where the object is stored. </p>

<p><strong>Additional Resources:</strong></p>

<ul>
<li><a href="https://developer.apple.com/documentation/swift/array" target="_blank">Array</a></li>
<li><a href="https://developer.apple.com/documentation/swift/contiguousarray" target="_blank">ContiguousArray</a></li>

