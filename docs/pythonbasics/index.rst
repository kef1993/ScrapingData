
Python Basics
=============

This section introduces some of the most relevant aspects of working
with Python for social scientists. This includes the different data
types available and ways to modify them.

**Be sure to execute each of the Python code cells as you read the
notebook.**

According to Wikipedia,

   Caribbean reef squid have been shown to communicate using a variety
   of color, shape, and texture changes.

To store that in Python, create a new variable called ``sentence``

.. code:: ipython3

    sentence =  'Caribbean reef squid have been shown to communicate using a variety of color, shape, and texture changes.'

The text is surrounded by a single quote (``'``) on each side. To make
sure that you typed the tweet correctly, you can type ``sentence``:

.. code:: ipython3

    sentence

You can get almost the same response using the ``print`` function:

.. code:: ipython3

    print(sentence)

The only difference is that the first response was wrapped in single
quotes and the second wasn’t. As a side note, the single quotes weren’t
because you put them there. If you used double quotes, Python would
still show a single-quote.

.. code:: ipython3

    sentence =  "Caribbean reef squid have been shown to communicate using a variety of color, shape, and texture changes."
    
    sentence

In addition to ``'`` and ``"``, strings can also be marked with a
``'''``. This last one is particularly useful when your text contains
contractions or quotation marks.

.. code:: ipython3

    new_sentence = '''According to Wikipedia, "Caribbean reef squid have been shown to communicate using a variety of color, shape, and texture changes."'''

.. code:: ipython3

    print(new_sentence)

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Create a new string called food that is a sentence about your most
recent meal. Display the contents of your new string.


.. raw:: html

   <details>

Sample answer code food = ‘I had a pizza for lunch.’ print(food)

.. raw:: html

   </details>

Strings
^^^^^^^

Python has a few tools for manipulating text, such as ``lower`` for
making the string lower-case.

.. code:: ipython3

    sentence.lower()

This did not alter the original string, however.

.. code:: ipython3

    sentence

In Python, strings are immmutable, meaning once created, they can not be
altered in place. We could store the results in a new variable.

.. code:: ipython3

    lower_sentence = sentence.lower()
    
    lower_sentence

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Create a new, lower cased version of your food string.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code food_lower = food.lower()

.. raw:: html

   </details>

We can also ``replace`` text within the string.

.. code:: ipython3

    sentence.replace("Caribbean reef squid", "Velociraptors")

``replace`` can also be used to remove text without replacement.

.. code:: ipython3

    sentence.replace(".", "")

As before, this does not alter the original string. If you wanted to
save the string edits, you would need to create a new variable.

.. code:: ipython3

    edited_sentence = sentence.lower()
    print(edited_sentence)

If you were doing a series of manipulations, you could reuse a varaiable
name, although it is best practices to keep a version of the original
string in case you ever need to go back to it.

.. code:: ipython3

    edited_sentence = sentence.lower()
    print(edited_sentence)
    
    edited_sentence = edited_sentence.replace(".", "")
    print(edited_sentence)

You can also stack multiple transformations together, although combining
too many may make your code harder to follow.

.. code:: ipython3

    edited_sentence.replace(".", "").lower()

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Create a new string called boring that removes the exclamation marks and
capitalization from the sentence “Way to go!!!”.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code

boring = “Way to go!!!”.replace(‘!’,’’).lower() print(boring)
Alternatively:

exciting = “Way to go!!!”.replace(‘!’,’‘) boring =
exciting.replace(’!‘,’’) boring = boring.lower() print(boring)

.. raw:: html

   </details>

Slicing
~~~~~~~

If you had a very long text, such as the entire text of a Wikipedia
article, you might only want to look at the first few characters. In
Python, this is called by slicing.

.. code:: ipython3

    sentence

.. code:: ipython3

    sentence[0:20]

A slice is signaled with brackets (``[]``). The first number is the
starting position, where 0 indicates the beginning. This is followed by
a colon (``:``) and then the end position, which, in this case, is a 20.
Note that this is splitting on characters, not words.

Here is a section from the middle of the string:

.. code:: ipython3

    sentence[20:32]

For convience, if you ommit the number before the colon, it defaults to
the string beginning.

.. code:: ipython3

    sentence[:40]

Ommitting the second number defaults to the end.

.. code:: ipython3

    sentence[40:]

Finally, negative numbers are interpreted as distance from the end of
the string.

.. code:: ipython3

    sentence[-20:]

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Create a new string called s that contains The weather is hot and humid
today. Find the slices for each of the following :

.. raw:: html

   <ul>

.. raw:: html

   <li>

The we

.. raw:: html

   <li>

today.

.. raw:: html

   <li>

hot and humid

.. raw:: html

   </ul>

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code s = ‘The weather is hot and humid today.’
print(s[:6]) print(s[-6:]) print(s[15:-7])

.. raw:: html

   </details>

Numbers
^^^^^^^

We can also count the number of characters in a string with the ``len``
function.

.. code:: ipython3

    len(sentence)

In this case, Python returned an interger instead of string. This also
can be stored in a variable.

.. code:: ipython3

    sentence_length = len(sentence)

.. code:: ipython3

    sentence_length

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

What is the length of How many dogs do you own?? Store it in a variable
called sl.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code sl = len(‘How many dogs do you own?’) print(sl)

.. raw:: html

   </details>

Since this is a number, we can do standard math operations with it.

.. code:: ipython3

    print(sentence_length * 3)

.. code:: ipython3

    print(sentence_length / 2)

.. code:: ipython3

    print(sentence_length + sentence_length)

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

What is one-third the length of sl.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code print(sl/3)

.. raw:: html

   </details>

As with strings, these can be saved in new variables.

.. code:: ipython3

    double_length = sentence_length + sentence_length
    
    print(double_length)

These same operators also work with strings.

.. code:: ipython3

    print(sentence * 2)

.. code:: ipython3

    print(sentence + sentence)

The operators can’t be used to combine different data types, however.

.. code:: ipython3

    print("The sentence was " + sentence_length + "characters.")

Conviently, Python the ``str`` function will convert an interger to a
string.

.. code:: ipython3

    print("The sentence was " + str(sentence_length) + " characters.")

I manually had to include the spaces before and after
``sentence_length``. Otherwise, it all is smushed together.

.. code:: ipython3

    print("The sentence was" + str(sentence_length) + "characters.")

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Print The length of the word “hippopotamus” is [x]. where [x] is the
length of the word hippopotamus .

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code l = len(‘hippopotamus’) s = ‘The length of the word
“hippopotamus” is’ + str(l) + ‘.’ print(s)

.. raw:: html

   </details>

Lists
^^^^^

We can also ``split`` the sentence into a series of strings. By default,
this splits based on spaces and other whitespace characters such as a
line break (``\n``) or tab character (``\t``).

.. code:: ipython3

    print(sentence.split())

What is returned here is a third data type (the first two were strings
and intergers) called a list. A list is enclosed in brackets (``[]``)
and the items are seperated by commas. In this case each item is in
quotation marks because they are all strings. Items in a list, however,
can be of any sort.

.. code:: ipython3

    my_list = ['Speeches', 7, 'Data']
    my_list

While ``len`` returned the number of characters in a string, it returns
the number the items in a list.

.. code:: ipython3

    len(my_list)

.. code:: ipython3

    sentence_length = len(sentence.split())
    sentence_length

In the second example, the list created by ``sentence.split()`` is not
saved in any way; only its length.

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Create a list called food that includes at least three things you ate
today. Use len to count the number of items in the list.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code food = [‘pizza slice’, ‘naan’, ‘cupcake’, ‘grape’]
print(len(food))

.. raw:: html

   </details>

Like, strings, lists can also be sliced. The first three items of a
list:

.. code:: ipython3

    words = sentence.split()
    print(words[:3])

We can also extract specific items from a list by their position. As it
did with strings, slicing in Python starts with 0.

.. code:: ipython3

    words[0]

The third word:

.. code:: ipython3

    words[3]

The fifth word from the end:

.. code:: ipython3

    words[-5]

The last two words, returned as a list:

.. code:: ipython3

    words[-2:]

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Display the first two items of your food list. What is the last item?

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code print(food[:2]) print(food[-1])

.. raw:: html

   </details>

Unlike a string, lists are mutable. That means that we can remove or as
is more frequently the case text analysis, add things to it. This is
done with ``append``.

.. code:: ipython3

    male_words = ['his', 'him', 'father']
    male_words.append('brother')
    print(male_words)

Since ``append`` is changing ``male_words``, we do not want to use an
``=``. The Python interpreter is editing our original list but not
returning anything.

.. code:: ipython3

    not_going_to_work = male_words.append('brother')
    print(not_going_to_work)

Lists can be also be combined using ``+``.

.. code:: ipython3

    gendered_words = male_words + ['her', 'she', 'mother']
    print(gendered_words)

As note above, the items in a list can include a variety of data types.
This includes lists.

.. code:: ipython3

    gendered_lists = [ male_words ,  ['her', 'she', 'mother'] ]

Note the two closing brackets next to each other. The first closes the
list that ends with ‘mother’ while the second closes our
``gendered_lists``.

.. code:: ipython3

    len(gendered_lists)

``gendered_lists`` has a length of two because it contains just two
items, each a list of varying lengths.

.. code:: ipython3

    print(gendered_lists)

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Add three more items to your foodlist. Use append for the first item.
For the other two, place them in a new list and then combine the two
lists.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code food.append(‘panini’) print(food) food = food +
[‘burrito’, ‘box of donuts’] print(food) print(len(food))

.. raw:: html

   </details>

Dictionaries
^^^^^^^^^^^^

A fourth useful data type is a dictionary. A dictionary is like a list
in that it holds multiples items. The items in a list can be identified
by their position in the list. In contrast, the values in a dictionary
are associated with a keyword. The analogy here is a to a physical
dictionary, which has a list of unique words, and each word has a
definition. In this case, the entries are called keys, and the
definitions, which can be any data type, are called values.

Alternatively, you can think of a dictionary as a single row of data
from a dataset, where the keys are the variable names.

.. code:: ipython3

    respondent = {'sex'   : "female",
                  'abany' : 1,
                  'educ'  : 'College'}

Dictionaries are surrounded by curly brackets (``{}``). Each entry is
pair consisting of the key, which must be a string, followed, by a colon
and then the value. Like in a list, entries are seperated by commas.

We can access the contents of a dictionary by enclosing the key in
brackets (``[]``).

.. code:: ipython3

    respondent['sex']

If the key is not dictionary, you will get a ``KeyError``.

.. code:: ipython3

    respondent['gender']

You can inspect all the keys in a dictionary, in case you forgot or
someone else made it.

.. code:: ipython3

    respondent.keys()

.. code:: ipython3

    len(respondent.keys())

Dictionaries are mutable, so we can change the value of existing keys,
remove keys, or add new ones.

.. code:: ipython3

    respondent['race'] = 'Black'
    
    print(respondent)

.. code:: ipython3

    respondent['abany'] = 'Yes'
    
    print(respondent)

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Add a new key to the dictionary called age with a value of 37. Confirm
that you did it correctly by dispaying the value of age.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code respondent[‘age’] = 37 print(respondent[‘age’])

.. raw:: html

   </details>

As noted above, while the keys have to be strings, the values can be any
data type.

.. code:: ipython3

    respondent['children ages'] = [3, 5, 10]
    
    print(respondent)

Spaces
^^^^^^

Within the Python community, there are strong norms about how code
should be written. Many of these are centered around have code be
readable, both by others and by your future self. As a trivial example,
``2+2`` is allowed, but is almost always written ``2 + 2``. Likewise, I
defined my respondent dictionary with plenty of white space to maximize
readability.

.. code:: ipython3

    respondent = {'sex'   : "female",
                  'abany' : 1,
                  'educ'  : 'College'}

This is identical to:

.. code:: ipython3

    respondent={'sex':'female','abany':1,'educ':'College'}


but putting it all on one line obscures the logic of the dictionary. In
this case, what is a key and what is a value is quite clear in the first
version, while distinguishing between the two is more problematic in the
single-line version.

.. code:: ipython3

    r2 = {'sex':'male',   'abany':1, 'educ':'College'     }
    r3 = {'sex':'female', 'abany':0, 'educ':'High School' }
    r4 = {'sex':'male',   'abany':0, 'educ':'Some College'}

.. code:: ipython3

    respondents = [respondent, r2, r3, r4]

.. code:: ipython3

    respondents

This now looks a lot like the common data format JSON!

Loops
~~~~~

.. code:: ipython3

    for person in respondents:
        print(person['educ'])

.. code:: ipython3

    for item in [1,2,'bobcat']:
        print(item)

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Loop over the items in your food list. For each item, print its length.

.. raw:: html

   </div>


.. raw:: html

   <details>

Sample answer code for item in food: item_len = len(item)
print(item_len)

.. raw:: html

   </details>

Functions
~~~~~~~~~

For those who come from Stata or R background, one of the more striking
aspects of Python code is the frequency of user-defined functions. These
functions are deployed both for cases where you are surprised that no
one has already written a function, such as counting words in a
sentence, and for highly-custom situations, such as scraping the
contents of a particular web page. Programming with many small functions
tends to make code more readable and easier to debug than code written
in a more traditional social science style.

A standard function has three parts. First, the function is named.
Subsequent lines or lines do the thing. Finally, the results are
returned.

A trivial function that returns the ``Hello!`` might look like:

.. code:: ipython3

    def make_hello():
        word = 'Hello!'
        return word

Of note, ``def`` signals that your are defining a function. This is
followed by the name of the function. In this case, ``make_hello``.
Since this function doesn’t take any arguments, such as accepting a
variable to modify or have any options, it is followed by ``()``. The
first line ends with a colon.

All subsequent lines are indented. The second line creates a new string
variable called ``word`` which contains ``Hello!``. The third and final
line of the functions returns the value stored in word.

.. code:: ipython3

    make_hello()

More commonly in text analysis, a user-defined function modifies an
existing string. In this case, the variable name that will be used
within the function is established within the parenthesis on the opening
line.

A second trivial function takes a text string and returns an all-caps
version.

.. code:: ipython3

    def scream(text):
        text_upper = text.upper()
        return text_upper

.. code:: ipython3

    scream('Hi there!')

|image0|

.. |image0| image:: https://raw.githubusercontent.com/nealcaren/UiOBigData/master/notebooks/images/function.png

The ``text`` and ``text_upper`` variable only exist within the function.
That means that you can pass a variable not called ``text`` to the
function.

.. code:: ipython3

    scream(sentence)

It also means that everything but the returned ``text`` disappears.

.. code:: ipython3

    text_upper

It is a good idea to include a comment within the function that explains
the function. This is helpful for other people reading your code and
when you return to your own code months and days later.

.. code:: ipython3

    def scream(text):
        '''Returns an all-caps version of text string.'''
        text_upper = text.upper()
        return text_upper

.. raw:: html

   <div class="alert alert-info">

.. raw:: html

   <h3>

Your turn

.. raw:: html

   </h3>

.. raw:: html

   <p>

Make a function call “whisper” that replaces all exclamation marks with
a period and returns a lower case version of a string. Test it out.

.. raw:: html

   </div>

.. code:: ipython3

    def whisper(text):
        ''''''
        
        return quiet_text

.. raw:: html

   <details>

Sample answer code def whisper(text): ’‘’Lower case string and replace !
with .’’’ quiet_text = text.replace(‘!’,‘.’) quiet_text =
quiet_text.lower() return quiet_text

Testing it out: whisper(‘ASDFASDFAS!’)

.. raw:: html

   </details>

Congratulations! You’ve now been introduced to the basics of Python for
social scientists.
