Python
======

# iter()
# partial() - takes an optional sentinel value

- looping inside list of number
for i in [0, 1, 2, 3, 4, 5]:
    print i**2

for i in range(6):
    print i**2

- Looping over a collection
for color in colors:
    print color

- looping backwards
for color in reverserd(colors):
    print color

looping over a collection and indices
for i, color in enumrate(colors):
    print i, '-->', colors

# looping over two collection
name = ['raymond', 'rachel', 'matthew']
colors = ['red', 'green', 'blue', 'yellow']

for name, color in izip(names, colors):
    print name, '-->', color

# looping in sorted order
colors = ['red', 'green', 'blue', 'yellow']

for color in sorted(colors):
    print(color)

for color in sorted(colors, reverse=True):
    print color

# custom sort order
colors = ['red', 'green', 'blue', 'yellow']

def compare_length(c1, c2):
    if len(c1) < len(c2): return -1
    if len(c1) > len(c2): return 1
    return 0

print sorted(colors, cmp=compare_length)
print sorted(colors, key=len)

# Distinguishing multiple exit points in loops

def find(seq, target):
    for i, value in enumerate(seq):
        if value == target:
	    break
    else:
        return -1
    return i

# Looping over dictionnaries
d = {'matthew': 'blue', 'rachel': 'green', 'raymond': 'red'}

for k in d:
    print k

for k in d.keys():
    if k.startswidth('r'):
        del d[k]

# Looping over a dictionnary keys and values
for k in d:
    print k, '-->', d[k]

for k, v in d.items():
    print k, '-->', v

# construct a dictionnary from pairs
names = ['raymond', 'rachel', 'mattew']
colors = ['red', 'green', 'blue']

d = dict(izip(names, colors))
{'matthew': 'blue', 'rachel': 'green', 'raymond': 'red'}

d = dict(enumerate(names))
{0: 'matthew', 1: 'rachel', 2: 'raymond'}



- defaultdict()
- d.popitem()
- argparse
- dict.update()
- ChainMap(d3, d2, default)
- namedtuple()
- unpacking sequences
name, age, size, id = s

- multiple state variable
x, y = y, x+y

- join sequences
print ', '.join(names)

- deque ?

- getcontext()

width ignored(OSError):
    os.remove('somefile.tmp')

@contextmanager
def ignored(*exceptions):
    try:
        yield
    except exceptions:
        pass:w

VIM
===
Sessions in Vim. For smart vim reloading.
xolox/vim-session

Fuzzy file finder
ctrlp

vim-vinegar ?? like nerdtree ?

Plugins manager
gmarik/vundle

