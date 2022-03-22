#include <iostream>

using namespace std;

struct citas
{
	char nombre[50];
	char tratamiento[50];
	char descripcion[50];
	int hora, minutos, preciounitt, tae, jk, total;
};
int main()
{
	int decision = 1, jmn, i, j, yng;
	citas pacientes[5];

	while (decision == 1)
	{
		cout << "BIENVENIDO AL MENU DE OPCIONES, POR FAVOR ELIGE UNA OPCION" << endl;
		cout << "1.-Agendar cita" << endl;
		cout << "2.-Modificar cita" << endl;
		cout << "3.-Eliminar cita" << endl;
		cout << "4.-Lista de citas vigentes" << endl;
		cout << "5.-Limpiar pantalla" << endl;
		cout << "6.-Salir" << endl;
		cin >> jmn;

		switch (jmn)
		{
		case 1:
			for (i = 0; i < 5; i++)
			{
				cout << "Numero de cita: " << i + 1 << endl;
				cout << "Ingrese el nombre del paciente" << endl;
				cin >> pacientes[i].nombre;
				cout << "Ingrese la hora del tratamiento" << endl;
				cin >> pacientes[i].hora;
				cin >> pacientes[i].minutos;
				cout << "Nombre del tratamiento" << endl;
				cin >> pacientes[i].tratamiento;
				cout << "Ingrese una descripcion" << endl;
				cin >> pacientes[i].descripcion;
				cout << "Precio unitario del tratamiento" << endl;
				cin >> pacientes[i].preciounitt;
				cout << "Cantidad del tratamiento" << endl;
				cin >> pacientes[i].tae;
				cout << "Precio unitario" << endl;
				cin >> pacientes[i].jk;
				//total = tae * jk;
				cout << "El total es: " << endl;
				cin >> pacientes[i].total;
			}
			break;



		case 2:
			cout << "ingrese el numero registro";
			cin >> j;
			j = j - 1;
			cout << "ingrese que desea modificar" << endl;
			cout << "1.-Editar nombre del paciente, 2.- Editar hora del paciente" << endl;
			cin >> yng;

			switch (yng)
			{
			case 1:
				for (i = j; i <= j; i++)
				{
					cout << "Numero de cita: " << i + 1 << endl;
					cout << "Ingrese el nombre del paciente" << endl;
					cin >> pacientes[i].nombre;
				}
				break;
			case 2:
				for (i = j; i <= j; i++)
				{
					cout << "Numero de cita: " << i + 1 << endl;
					cout << "Ingrese la hora del tratamiento" << endl;
					cin >> pacientes[i].hora;
					cin >> pacientes[i].minutos;
				}
				break;
			}
			break;



		case 3: //eliminar cita
			break;



		case 4:
			for (i = 0; i < 5; i++)
			{
				cout << "Numero de registro" << i + 1 << endl;
				cout << pacientes[i].nombre << endl;
				cout << pacientes[i].hora << endl;
				cout << pacientes[i].minutos << endl;
				cout << pacientes[i].tratamiento << endl;
				cout << pacientes[i].descripcion << endl;
				cout << pacientes[i].preciounitt << endl;
				cout << pacientes[i].tae << endl;
				cout << pacientes[i].jk << endl;
				cout << pacientes[i].total << endl;
			}
			break;


		case 5: //limpiar pantalla
			break;


		case 6:
			exit(EXIT_SUCCESS);
			decision = 2;
			break;

		default:
			cout << "opcion invalida";
		}
	}
}
