How to Import File from outside root dir

    import sys
    current = os.getcwd()
	sys.path.insert(0, current+'../support')

	import file