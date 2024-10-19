lib/*.o:src/*.c
	gcc -c $< -o $@ -I ./include
lib/libcal.a:lib/*.o
	ar rcs lib/libcal.a $<
main:main.c lib/libcal.a 
	gcc -o $@ $< -l cal -L lib -I ./include
.PHONY:clean
clean:
	rm -f lib/*.o:rm main
