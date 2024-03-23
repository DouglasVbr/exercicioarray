# exercicioarray

exercicio 4
package testearrayliststring;
import java.util.ArrayList;
import java.util.Collections;
import javax.swing.JOptionPane;
public class TesteArrayListString {
public static void main(String[] args) {
ArrayList<String> listaStrings = new ArrayList<>();
// Adiciona 10 Strings informadas pelo usuário
for (int i = 0; i < 10; i++) {
String input = JOptionPane.showInputDialog("Digite uma string:");
listaStrings.add(input);
}
// Percorre e imprime os valores de cada String na lista
JOptionPane.showMessageDialog(null, "Elementos antes da ordenação:");
StringBuilder elementosAntesOrdenacao = new StringBuilder();
for (String str : listaStrings) {
elementosAntesOrdenacao.append(str).append("\n");
}
JOptionPane.showMessageDialog(null, elementosAntesOrdenacao);
// Ordena os objetos na lista
Collections.sort(listaStrings);
// Percorre e imprime os valores de cada String na lista ordenada
JOptionPane.showMessageDialog(null, "Elementos após a ordenação:");
StringBuilder elementosAposOrdenacao = new StringBuilder();
for (String str : listaStrings) {
elementosAposOrdenacao.append(str).append("\n");
}
JOptionPane.showMessageDialog(null, elementosAposOrdenacao);
}
}

exercicio 3

package maiormenorelementolista;

import javax.swing.JOptionPane;
import java.util.ArrayList;
public class MaiorMenorElementoLista {

public static void main(String[] args) {

ArrayList<Integer> lista = new ArrayList<>();
// Solicita ao usuário que insira os números
String input = JOptionPane.showInputDialog("Insira os números separados por
vírgula:");
// Divide a entrada do usuário em números individuais e adiciona à lista
String[] numerosString = input.split(",");
for (String numero : numerosString) {
lista.add(Integer.parseInt(numero.trim()));
}
// Encontra o maior e o menor elemento na lista
int maior = Integer.MIN_VALUE;
int menor = Integer.MAX_VALUE;
for (int num : lista) {
if (num > maior) {
maior = num;
}
if (num < menor) {
menor = num;
}
}
// Exibe os resultados usando JOptionPane
JOptionPane.showMessageDialog(null, "O maior elemento é: " + maior + "\nO
menor elemento é: " + menor);
}
}

exercicio 2

package removeelementosrepetidos;

import javax.swing.JOptionPane;
import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Set;
public class RemoveElementosRepetidos {

public static void main(String[] args) {
// Solicita ao usuário que insira os números separados por vírgula
String input = JOptionPane.showInputDialog("Insira os elementos separados
por vírgula:");
// Divide a entrada do usuário em elementos individuais e adiciona à lista
String[] elementosString = input.split(",");
List<String> lista = new ArrayList<>();
for (String elemento : elementosString) {
lista.add(elemento.trim());
}
// Remove elementos repetidos usando um conjunto (Set)
Set<String> conjunto = new HashSet<>(lista);
lista.clear();
lista.addAll(conjunto);
// Constrói uma string com os elementos únicos
StringBuilder resultado = new StringBuilder();
for (String elemento : lista) {
resultado.append(elemento).append(", ");
}
// Remove a vírgula extra no final da string, se houver
if (resultado.length() > 0) {
resultado.setLength(resultado.length() - 2);
}
// Exibe os resultados usando JOptionPane
JOptionPane.showMessageDialog(null, "Elementos únicos: " +
resultado.toString());
}
}

exercicio 1

package calculamedia;
import java.util.ArrayList;
import java.util.List;
import javax.swing.JOptionPane;

public class CalculaMedia {

public static void main(String[] args) {
// Solicita ao usuário que insira os números separados por vírgula
String input = JOptionPane.showInputDialog("Insira os números separados por
vírgula:");
// Divide a entrada do usuário em números individuais e adiciona à lista
String[] numerosString = input.split(",");
List<Double> numeros = new ArrayList<>();
for (String numero : numerosString) {
numeros.add(Double.parseDouble(numero.trim()));
}
// Calcula a média dos números
double soma = 0;
for (double num : numeros) {
soma += num;
}
double media = soma / numeros.size();
// Exibe o resultado usando JOptionPane
JOptionPane.showMessageDialog(null, "A média dos números é: " + media);
}
}
