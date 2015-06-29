TEX = pdflatex -shell-escape -interaction=batchmode -file-line-error
AUX_FILES = caratula.tex caratula.sty config.sty header.sty
AUX_FILES_TP1 = tp1.tex tp1\conclusiones.tex tp1\diagrama-contexto.tex tp1\discusion.tex tp1\escenarios.tex tp1\introduccion.tex tp1\modelo-objetivos.tex tp1\presunciones.tex tp1\vistas.tex
AUX_FILES_TP2 = tp2.tex tp2\actividad.tex tp2\casos-de-uso.tex tp2\conceptual.tex tp2\conclusion.tex tp2\fsm.tex tp2\informe.tex tp2\introduccion.tex tp2\ocl.tex

informe.pdf: informe.tex $(AUX_FILES_TP1) $(AUX_FILES_TP2) $(AUX_FILES)
	@( $(TEX) informe.tex && clear && $(TEX) informe.tex ) || ( rm -f informe.pdf && echo -e "\n\n\e[1;31m¡La compilación falló amigo!\e[0m">&2 )

clean:
	rm -f *.aux *.log *.out *.fdb_latexmk *.fls *.ilg *.ind *.idx *.toc *.synctex.gz

