
---

# 📘 Manual de Uso de Git

## 🔹 Preparación

Antes de comenzar, se recomienda verificar la instalación de Git con:

```powershell
git --version
```

Posteriormente, es necesario configurar la identidad del usuario:

```powershell
git config --global user.name "Nombre del usuario"
git config --global user.email "correo@ejemplo.com"
```

---

## 🔹 Crear o clonar un repositorio

* **Para clonar un repositorio ya existente en GitHub**:

  ```powershell
  git clone https://github.com/usuario/proyecto.git
  cd proyecto
  ```

* **Para iniciar un repositorio nuevo**:

  ```powershell
  mkdir proyecto; cd proyecto
  git init
  git remote add origin https://github.com/usuario/proyecto.git
  ```

> **origin** es el alias del remoto. Es un nombre por convención, aunque puede cambiarse.

---

## 🔹 Preparar para enviar

El ciclo básico de trabajo consiste en:

```powershell
git add .
git commit -m "Mensaje de commit"
```

---

## 🔹 Enviar cambios al remoto

La primera vez en una rama nueva (ejemplo: `main`):

```powershell
git push -u origin main
```

* El parámetro **`-u`** vincula la rama local con la remota (tracking).
* `main` se puede cambiar por la rama correspondiente.

Después, bastará con ejecutar:

```powershell
git push
```

---

## 🔹 Gestión de ramas

* **Listar ramas existentes**:

  ```powershell
  git branch
  ```

* **Crear y cambiar a una rama de trabajo**:

  ```powershell
  git checkout -b mirama
  # o
  git switch -c mirama
  ```

---

## 🔹 Fusionar una rama de trabajo en la principal

Para integrar la rama `mirama` dentro de `main`:

```powershell
git checkout main
git pull --ff-only
git merge mirama
git push
```

---

## 🔹 Comandos útiles de verificación

* **Estado actual**:

  ```powershell
  git status
  git status -sb
  ```

* **Seguimiento de ramas**:

  ```powershell
  git branch -vv
  ```

* **Historial gráfico**:

  ```powershell
  git log --oneline --graph --decorate --all
  ```

---

## 🔹 Obtener y aplicar cambios de inmediato

**pull = traer y mezclar 🔄**

```powershell
git pull
```

Este comando aplica los cambios directamente sobre la rama activa.

---

## 🔹 Cheat Sheet

* **Estado rápido**:

  ```powershell
  git status -sb
  ```

* **Actualizar y aplicar**:

  ```powershell
  git pull
  ```

* **Subir cambios**:

  ```powershell
  git push -u origin rama
  ```

* **Fusionar ramas**:

  ```powershell
  git checkout main
  git pull --ff-only
  git merge dev
  git push
  ```

* **Cancelar merge**:

  ```powershell
  git merge --abort
  ```

---

✅ Este manual funciona como una guía práctica para trabajar con Git: desde la configuración inicial hasta la gestión de ramas, sincronización con remoto y resolución de fusiones.

---


