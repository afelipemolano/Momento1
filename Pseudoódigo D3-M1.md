INICIO

// Desafio 3: Viabilidad de pedido mayorista complejo

//ENTRADA
// =========================

    // CONSTANTES (EN MAYUSCULA POR CONVENCIÓN)
    // =========================
    Definir CANTIDAD_MINIMA Como Entero
    Definir CAPACIDAD_MAXIMA_KG Como Real

    CANTIDAD_MINIMA <- 50
    CAPACIDAD_MAXIMA_KG <- 750
 
    //VARIABLES (Primera letra de la primera palabra en minúscula, en adelante la primera letra mayúscula)
    // =========================

    Definir precioUnitario Como Real
    Definir pesoUnitario Como Real
    Definir cantidadSolicitada Como Entero
    Definir saldoCliente Como Real

    Definir costoTotal Como Real
    Definir pesoTotal Como Real
    Definir esPedidoViable Como Logico


    Escribir "Ingrese el precio unitario del producto:"
    Leer precioUnitario

    Escribir "Ingrese el peso en kilogramos de una unidad:"
    Leer pesoUnitario

    Escribir "Ingrese la cantidad de unidades solicitadas:"
    Leer cantidadSolicitada

    Escribir "Ingrese el saldo disponible en la cuenta del cliente:"
    Leer saldoCliente


//PROCESO
// =========================

    costoTotal <- precioUnitario * cantidadSolicitada

    pesoTotal <- pesoUnitario * cantidadSolicitada

    esPedidoViable <- (cantidadSolicitada > CANTIDAD_MINIMA) Y (costoTotal <= saldoCliente) Y (pesoTotal <= CAPACIDAD_MAXIMA_KG)


// SALIDA
// =========================
    Escribir "Es ", esPedidoViable, "que el pedido es viable"

FIN