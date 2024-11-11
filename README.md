#include <iostream>
#include <string>

class Empleado {
private:
    std::string nombreEmpleado;
    double salarioMensualEmpleado;

public:
    // Constructor de la clase Empleado
    Empleado(const std::string& nombre, double salarioMensual) 
        : nombreEmpleado(nombre), salarioMensualEmpleado(salarioMensual) {}

    // Método para obtener el nombre del empleado
    std::string obtenerNombreEmpleado() const {
        return nombreEmpleado;
    }

    // Método para obtener el salario mensual del empleado
    double obtenerSalarioMensualEmpleado() const {
        return salarioMensualEmpleado;
    }

    // Método para calcular el salario anual del empleado
    double calcularSalarioAnualEmpleado() const {
        return salarioMensualEmpleado * 12;
    }

    // Método para mostrar la información completa del empleado
    void mostrarInformacionEmpleado() const {
        std::cout << "Nombre del Empleado: " << nombreEmpleado << std::endl;
        std::cout << "Salario Mensual del Empleado: $" << salarioMensualEmpleado << std::endl;
        std::cout << "Salario Anual del Empleado: $" << calcularSalarioAnualEmpleado() << std::endl;
    }
};

int main() {
    // Crear un objeto de la clase Empleado con el nombre y el salario mensual
    Empleado empleadoJuan("Juan Perez", 3000.0);

    // Mostrar la información completa del empleado
    empleadoJuan.mostrarInformacionEmpleado();

    return 0;
}

