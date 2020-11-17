Este directorio albergará los códigos desarrollados durante el curso como parte de las tareas y asignaciones

TALLER 3

/*INCISO A*/
load ("eigen")$
/*CARGAMOS LA LIBRERIA "eigen"*/
producto(f,g):=integrate(1,t,-1,1);
/*DEFINIMOS EL ESPACIO ENTRE (-1,1), Y DEFINIMOS EL PRODUCTO INTERNO*/
p:makelist(t^n,n,0,3)$;
/*ESTABLECEMOS EL NÙMERO DE ELEMENTOS DE NUESTRA POSIBLE BASE */
j:gramschmidt ([1,t,t^2,t^3,t^4],producto);
/*ORTOGONALIZAMOS LOS ELEMENTOS LA POSIBLE BASE*/
j:expand(%);
/*EXPANDIMOS LOS TERMINOS DE LA ORTOGONALIZACIÒN*/
map(producto,[j[1],j[2],j[4],j[3]],[j[2],j[3],j[1],j[4]]);
/*COMPROBAMOS QUE SEA ORTOGONAL "EFECTIVAMENTE NO LO SON"*/
/*INCISO B*/
load ("eigen")$
/*CARGAMOS LA LIBRERIA "eigen"*/
producto(f,g):=integrate(1,t,-1,1);
/*DEFINIMOS EL ESPACIO ENTRE (-1,1), Y DEFINIMOS EL PRODUCTO INTERNO*/
p:makelist(t^n,n,0,10)$;
/*ESTABLECEMOS EL NÙMERO DE ELEMENTOS DE NUESTRA POSIBLE BASE */
j:gramschmidt ([1,t,t^2,t^3,t^4,t^5,t^6,t^7,t^8,t^9,t^10],producto);
/*ORTOGONALIZAMOS LOS ELEMENTOS LA POSIBLE BASE*/
j:expand(%);
/*EXPANDIMOS LOS TERMINOS DE LA ORTOGONALIZACIÒN*/
map(producto,[j[1],j[2],j[3],j[4],j[5],j[6],j[7],j[8],j[9],j[10],j[11]],[j[11],j[10],j[9],j[8],j[7],j[6],j
[5],j[4],j[3],j[2],j[1]]);
/*COMPROBAMOS QUE SEA ORTOGONAL "EFECTIVAMENTE NO LO SON"*/


5 PUNTO
load ("eigen")$;
/*CARGAMOS LA LIBRERIA "eigen"*/
producto(f,g):=(integrate(f*g*sqrt(1-t^2),t,-1,1));
/*DEFINIMOS EL ESPACIO ENTRE (-1,1), Y DEFINIMOS EL PRODUCTO INTERNO*/
p:makelist(t^n,n,0,3)$;
/*ESTABLECEMOS EL NÙMERO DE ELEMENTOS DE NUESTRA POSIBLE BASE */
j:gramschmidt(p,producto)$;
/*ORTOGONALIZAMOS LOS ELEMENTOS LA POSIBLE BASE*/
expand(j)$;
/*EXPENDEMOS LOS TERMINOS DE LA ORTOGONALIZACIÒN*/
ratsimp(j);
/*SIMPLIFICAMOS LA EXPRESIÒN*/


6 PUNTO
load ("eigen")$;
/*CARGAMOS LA LIBRERIA "eigen"*/
producto(f,g):=(integrate(f*g/sqrt(1-t^2),t,-1,1));
/*DEFINIMOS EL ESPACIO ENTRE (-1,1), Y DEFINIMOS EL PRODUCTO INTERNO*/
p:makelist(t^n,n,0,3)$;
/*ESTABLECEMOS EL NÙMERO DE ELEMENTOS DE NUESTRA POSIBLE BASE */
j:gramschmidt(p,producto)$;
/*ORTOGONALIZAMOS LOS ELEMENTOS LA POSIBLE BASE*/
expand(j)$;
/*EXPENDEMOS LOS TERMINOS DE LA ORTOGONALIZACIÒN*/
ratsimp(j);
/*SIMPLIFICAMOS LA EXPRESIÒN*/
map(producto,[j[1],j[2],j[4],j[3]],[j[2],j[3],j[1],j[4]]);
/*COMPROBAMOS QUE SEA ORTOGONAL*/
map(producto,[j[1],j[2],j[4],j[3]],[j[2],j[3],j[1],j[4]]);
/*COMPROBAMOS QUE SEA ORTOGONAL*/

punto 3 parte d
load ("eigen")$
p:makelist(sen(3*t)*(1-t^2),t,0,10)$;
o:makelist(sen(3*t)*(1-t^2),t+1,0,10)$;
lagrange(p,o);
