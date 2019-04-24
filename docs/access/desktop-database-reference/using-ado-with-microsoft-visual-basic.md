---
title: Использование ADO с Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26eaa93a1abbb3778a2735d50dd5022edb3023d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306225"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Использование ADO с Microsoft Visual Basic

**Область применения**: Access 2013, Office 2013

Настройка проекта ADO и написание кода ADO аналогичны, независимо от того, используете ли вы Visual Basic или Visual Basic для приложений. В этом разделе рассматривается использование ADO вместе с Visual Basic и Visual Basic для приложений, а также заметок о различиях.

## <a name="referencing-the-ado-library"></a>Создание ссылок на библиотеку ADO

Проект ADO должен ссылаться на библиотеку ADO.

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>Ссылка на ADO из Microsoft Visual Basic

1. В Visual Basic в меню **проект** выберите **ссылки...**.

2. Выберите **библиотеку Microsoft ActiveX Data Objects x. x** из списка. Убедитесь, что также выбраны по крайней мере следующие библиотеки:
   
   - Visual Basic for Applications
   - Объекты и процедуры среды выполнения Visual Basic
   - Объекты и процедуры Visual Basic
   - OLE Automation

3. Нажмите кнопку **ОК**.

Вы можете использовать ADO так же, как и в Visual Basic для приложений, например, с помощью Microsoft Access.

### <a name="to-reference-ado-from-microsoft-access"></a>Ссылка на ADO из Microsoft Access

1. В Microsoft Access выберите или создайте модуль на вкладке **модули** окна **базы данных** .

2. В меню **Сервис** выберите пункт **ссылки..**..

3. Выберите **библиотеку Microsoft ActiveX Data Objects x. x** из списка. Убедитесь, что также выбраны по крайней мере следующие библиотеки:
    
   - Visual Basic for Applications
   - Библиотека объектов Microsoft Access 11,0 (или более поздней версии)

4. Нажмите кнопку **ОК**.

## <a name="creating-ado-objects-in-visual-basic"></a>Создание объектов ADO в Visual Basic

Чтобы создать переменную автоматизации и экземпляр объекта для этой переменной, можно использовать два метода: **Dim** или **CreateObject**.

### <a name="dim"></a>Dim

Вы можете использовать ключевое слово **New** с **Dim** для объявления и создания экземпляров объектов ADO за один шаг:

```vb 
 
Dim conn As New ADODB.Connection 
```

Кроме того, объявление оператора **Dim** и создание экземпляра объекта также могут быть двумя этапами:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> Нет необходимости явно использовать ProgID ADODB с оператором **Dim** , предполагая, что вы правильно ссылались на библиотеку ADO в проекте. Тем не менее, использование этого параметра гарантирует, что конфликты имен с другими библиотеками не будут.
> 
> Например, если вы включили в один проект ссылки на ADO и DAO, необходимо добавить квалификатор, указывающий, какую объектную модель использовать при создании экземпляров объектов **Recordset** , как показано в следующем коде:  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

При использовании метода **CreateObject** объявление и создание экземпляра объекта должны быть выполнены в два отдельных этапа:

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Объекты, создаваемые с помощью **CreateObject** , имеют тип с поздней привязкой, что означает, что они не являются строго типизированными, а завершение командной строки отключено. Тем не менее, это позволяет пропустить ссылку на библиотеку ADO из проекта и создать экземпляры определенных версий объектов. Пример:

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Это также можно сделать, специально создав ссылку на библиотеку типов ADO версии 2,0 и создав объект.

Создание экземпляров объектов с помощью метода **CreateObject** обычно выполняется медленнее, чем при использовании оператора **Dim** .

## <a name="handling-events"></a>Обработка событий

Для обработки событий ADO в Microsoft Visual Basic необходимо объявить переменную на уровне модуля с помощью ключевого слова **WithEvents** . Переменная может быть объявлена только как часть модуля класса и должна быть объявлена на уровне модуля. Более подробное описание обработки событий ADO приведено в [главе 7: обработка событий ADO](chapter-7-handling-ado-events.md).

## <a name="visual-basic-examples"></a>Примеры Visual Basic

Многие примеры Visual Basic включены в документацию по ADO. Дополнительные сведения приведены [в статье примеры кода ADO в Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).

