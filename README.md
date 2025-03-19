# Cajero
Andy Cardona Paz. Carne: 1625125

Codigo:

    def cajero_automatico():
        saldo = 3000
        intentos = 0
        max_intentos = 3
    
    while saldo > 0:
        print(f"Saldo actual: Q{saldo}")
        try:
            monto = int(input("Ingrese monto a retirar (o '0' para salir): "))
            
            if monto == 0:
                print("Gracias por usar el cajero. Adiós.")
                break
            
            if monto > saldo:
                intentos += 1
                print(f"Saldo insuficiente. Intentos restantes: {max_intentos - intentos}")
                if intentos >= max_intentos:
                    print("Demasiados intentos fallidos. Operación cancelada.")
                    break
            else:
                saldo -= monto
                print(f"Retiro exitoso. Nuevo saldo: Q{saldo}")
                
                if saldo == 0:
                    print("Saldo agotado. Adiós.")
                    break
        
        except ValueError:
            print("Entrada inválida. Por favor, ingrese un número válido.")

          # Ejecutar
          cajero_automatico()
