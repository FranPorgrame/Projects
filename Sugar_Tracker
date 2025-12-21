#Datos de persona
import time
while True:
 edad = int(input("Cuantos años tienes? (1-100): "))
 if 1 <= edad <= 100:
     print(f"Edad registrada: {edad} años")
     break

while True:
    peso = float(input("Cuanto pesas? (30-200 kg): "))

    if 30 <= peso <= 200:
        print(f"El peso fue registrado: {peso} kg")
        break

while True:
    estatura = float(input("Cuanto mides? (0-200 cm): "))
    if 0 <= estatura <= 200:
        print(f"La estatura fue registrado: {estatura} cm")
        break

while True:
    sexo = input("Ingresa el sexo (M/F): ").upper()
    if sexo == "M":
        print(f"El sexo fue registrado correctamente: {sexo}")
        break
    if sexo == "F":
        print(f"El sexo fue registrado correctamente: {sexo}")
        break

mensaje = "Procesando..."
duracion_total = 5 # segundos
intervalo = 2 # segundos
inicio = time.time()

while time.time() - inicio < duracion_total:
    print(mensaje)
    time.sleep(intervalo)

#Cálculo de gasto energetico minimo
tmb_male = (float(10 * peso) + (6.25 * estatura) - (5 * edad) + 5)
tmb_female = (float(10 * peso) + (6.25 * estatura) - (5 * edad) - 161)

def calc_min_f(sexo, estatura, peso, edad):
    if sexo == "M":
        print(f"Su TMB(Tasa Metabolica Basal) o consumo minimo, es de {tmb_male:.2f} kcal")
        print("")
    elif sexo == "F":
        print(f"Su TMB(Tasa Metabolica Basal) o consumo minimo, es de {tmb_female:.2f} kcal")
        print("")
    return

#GET PARA HOMBRE
get_male_bajo = tmb_male * 1.2
get_male_mode = tmb_male * 1.55
get_male_alto = tmb_male * 1.725

#GET PARA MUJER
get_female_bajo = tmb_female * 1.2
get_female_mode = tmb_female * 1.55
get_female_alto = tmb_female * 1.725

print("")
calc_min_f(sexo, estatura, peso, edad)

while True:
    actividad_fisica = input("Cuanta actividad fisica haces? (Poco, Moderado, Alto): ").capitalize()
    if sexo == "M" and actividad_fisica == "Poco":
        print(f"Su GET(Gasto Energetico Total Diario) es de {get_male_bajo:.2f} kcal")
        break
    if sexo == "F" and actividad_fisica == "Poco":
        print(f"Su GET(Gasto Energetico Total Diario) es de {get_female_bajo:.2f} kcal")
        break
    if sexo == "M" and actividad_fisica == "Moderado":
        print(f"Su GET(Gasto Energetico Total Diario) es de {get_male_mode:.2f} kcal")
        break
    if sexo == "F" and actividad_fisica == "Moderado":
        print(f"Su GET(Gasto Energetico Total Diario) es de {get_female_mode:.2f} kcal")
        break
    if sexo == "M" and actividad_fisica == "Alto":
        print(f"Su GET(Gasto Energetico Total Diario) es de {get_male_alto:.2f} kcal")
        break
    if sexo == "F" and actividad_fisica == "Alto":
        print(f"Su GET(Gasto Energetico Total Diario) es de {get_female_alto:.2f} kcal")
        break

print("")
#Calculo para BAJAR peso
hom_bajar_pocaAct = get_male_bajo - 500
hom_bajar_modeAct = get_male_mode - 500
hom_bajar_altoAct = get_male_alto - 500

muj_bajar_pocaAct = get_female_bajo - 500
muj_bajar_modeAct = get_female_mode - 500
muj_bajar_altoAct = get_female_alto - 500
#Para MANTENER peso se print el GET (no cambia)

#Calculo para AUMENTAR peso
hom_aum_pocaAct = get_male_bajo + 500
hom_aum_modeAct = get_male_mode + 500
hom_aum_altoAct = get_male_alto + 500

muj_aum_pocaAct = get_female_bajo + 500
muj_aum_modeAct = get_female_mode + 500
muj_aum_altoAct = get_female_alto + 500
frase = 'Su consumo diario deberia ser de: '
def fun_print_M_bajar(actividad_fisica, sexo):
    if sexo == "M":
        if actividad_fisica == "Moderado":
            print(f"{frase} {hom_bajar_modeAct:.2f}kcal")
        elif actividad_fisica == "Poco":
            print(f"{frase} {hom_bajar_pocaAct:.2f}kcal")
        elif actividad_fisica == "Alto":
            print(f"{frase} {hom_bajar_altoAct:.2f}kcal")
    else:
        if actividad_fisica == "Moderado":
            print(f"{frase} {muj_bajar_modeAct:.2f}kcal")
        elif actividad_fisica == "Poco":
            print(f"{frase} {muj_bajar_pocaAct:.2f}kcal")
        elif actividad_fisica == "Alto":
            print(f"{frase} {muj_bajar_altoAct:.2f}kcal")
    return

def fun_print_M_mantener(actividad_fisica, sexo):
    if sexo == "M":
        if actividad_fisica == "Poco":
            print(f"{frase} {get_male_bajo:.2f}kcal")
        elif actividad_fisica == "Moderado":
            print(f"{frase} {get_male_mode:.2f}kcal")
        elif actividad_fisica == "Alto":
            print(f"{frase} {get_male_alto:.2f}kcal")
    else:
        if actividad_fisica == "Poco":
            print(f"{frase} {get_female_bajo:.2f}kcal")
        elif actividad_fisica == "Moderado":
            print(f"{frase} {get_female_mode:.2f}kcal")
        elif actividad_fisica == "Alto":
            print(f"{frase} {get_female_alto:.2f}kcal")
        return

def fun_print_M_subir(actividad_fisica, sexo):
    if sexo == "M":
        if actividad_fisica == "Poco":
            print(f"{frase} {hom_aum_pocaAct:.2f}kcal")
        elif actividad_fisica == "Moderado":
            print(f"{frase} {hom_aum_modeAct:.2f}kcal")
        elif actividad_fisica == "Alto":
           print(f"{frase} {hom_aum_altoAct:.2f}kcal")
    else:
        if actividad_fisica == "Poco":
            print(f"{frase} {muj_aum_pocaAct:.2f}kcal")
        if actividad_fisica == "Moderado":
            print(f"{frase} {muj_aum_modeAct:.2f}kcal")
        if actividad_fisica == "Alto":
            print(f"{frase} {muj_aum_altoAct:.2f}kcal")
        return

while True:
    peso_deseado = input("Desea bajar, subir, o mantener su peso actual?").lower()
    if sexo == 'M':
        if peso_deseado == "bajar":
            fun_print_M_bajar(actividad_fisica, sexo)
        elif peso_deseado == "subir":
            fun_print_M_subir(actividad_fisica, sexo)
        elif peso_deseado == "mantener":
            fun_print_M_mantener(actividad_fisica, sexo)
        break
    else:
        if peso_deseado == "bajar":
            fun_print_M_bajar(actividad_fisica, sexo)
        elif peso_deseado == "subir":
            fun_print_M_subir(actividad_fisica, sexo)
        elif peso_deseado == "mantener":
            fun_print_M_mantener(actividad_fisica, sexo)
        break

frase2 = print("El valor que se muestra a continuacion es su consumo de azucar maximo expresado en kcal y gr de azucar: ")

def calc_azu_kcal(sexo, actividad_fisica):
    if sexo == "M":
        if actividad_fisica == "Poco":
            print(f"{frase2}")
            fun_print_M_bajar(actividad_fisica, sexo) * 0.10
            fun_print_M_bajar(actividad_fisica, sexo) * 0.10 / 4
        elif actividad_fisica== "Moderado":
            print(f"{frase2}")
            fun_print_M_subir(actividad_fisica, sexo) * 0.10
            fun_print_M_subir(actividad_fisica, sexo) * 0.10 / 4
        elif actividad_fisica== "Alto":
            print(f"{frase2}")
