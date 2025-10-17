La realizacion del punto 3 se realiza desde SQLiteStudio.
En entorno local realizarlos antes.

a) Insertar un Producto
```
    INSERT INTO Productos (Descripcion, Precio) VALUES ('Teclado HyperX Alloy Fps',98700.0);
    INSERT INTO Productos (Descripcion, Precio) VALUES ('Adaptador Bluetooth',5000.0);
    INSERT INTO Productos (Descripcion, Precio) VALUES ('Switch Cherry MX Red (unidad)',2200.0);
```
b) Insertar un Presupuesto
```sql
    INSERT INTO Presupuestos (NombreDestinatario, FechaCreacion) VALUES ('Solomon Jedidas', '2025-10-17');
    INSERT INTO Presupuestos (NombreDestinatario, FechaCreacion) VALUES ('Baltasar Gracian', '2025-10-17');
    INSERT INTO Presupuestos (NombreDestinatario, FechaCreacion) VALUES ('Pierre Simon Laplace', '2025-10-17'); 
```
c) Insertar registros en PresupuestoDetalle
```sql
    INSERT INTO PresupuestosDetalle (idPresupuesto, idProducto, Cantidad) VALUES (1, 1, 25);
    INSERT INTO PresupuestosDetalle (idPresupuesto, idProducto, Cantidad) VALUES (2, 2, 3);
    INSERT INTO PresupuestosDetalle (idPresupuesto, idProducto, Cantidad) VALUES (3, 3, 2);
```
d) Modificar un Producto 
    **El id depende del orden en el que se cargo, en la version local de la facultad es el 3**
```sql
    UPDATE Productos SET Descripcion = 'Teclado HyperX Alloy FPS', Precio = 95000 WHERE idProducto = 3; 
```

e) Modificar NombreDestinatario de Presupuesto
    **El id depende del orden en el que se cargo, en la version local de la facultad es el 1**
```sql
    UPDATE Presupuestos SET NombreDestinatario = 'Pierre-Simon Laplace' WHERE idPresupuesto = 1; 
```

f) Eliminar un registro de PresupuestoDetalle
    **El id depende del orden en el que se cargo, en la version local de la facultad es el 1**
    `Laplace aint buying any switches today`
```sql    
    DELETE FROM PresupuestosDetalle WHERE idPresupuesto = 1 AND idProducto = 1;
```
