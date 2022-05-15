# median of products
import statistics
def sfunction(indice):
 s0=290797
 answer=[290797]
 for x in range(0,indice-1):
  s=(s0**2)%50515093
  answer.append(s)
  s0=s
 return answer 
def multiplicacion(n):
  a=sfunction(n)
  solucion=[]
  for x in range(len(a)):
     for i in range(len(a)):
       if x<i:
        multi=a[x]*a[i]
        solucion.append(multi)
  return solucion
print(statistics.median(multiplicacion(1000003)))
