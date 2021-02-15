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

Настройка проекта ADO и написание кода ADO аналогично независимо от того, Visual Basic или Visual Basic для приложений. В этом разделе используется ADO с Visual Basic и Visual Basic для приложений и отмечаются все различия.

## <a name="referencing-the-ado-library"></a>Ссылка на библиотеку ADO

На библиотеку ADO должен ссылаться ваш проект.

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>Ссылка на ADO из Microsoft Visual Basic

1. В Visual Basic выберите в меню **"Проект"** **ссылки...**

2. Выберите **microsoft ActiveX объектов данных x.x в** списке. Убедитесь, что выбраны по крайней мере следующие библиотеки:
   
   - Visual Basic for Applications
   - Visual Basic и процедуры времени работы
   - Visual Basic объектов и процедур
   - OLE Automation

3. Нажмите **ОК**.

Вы можете использовать ADO так же легко с Visual Basic для приложений, например с помощью Microsoft Access.

### <a name="to-reference-ado-from-microsoft-access"></a>Ссылка на ADO из Microsoft Access

1. В Microsoft Access выберите или создайте модуль на вкладке **"Модули"** в **окне "База данных".**

2. В меню **"Инструменты"** выберите **ссылки...**

3. Выберите **microsoft ActiveX объектов данных x.x в** списке. Убедитесь, что выбраны по крайней мере следующие библиотеки:
    
   - Visual Basic for Applications
   - Библиотека объектов Microsoft Access 11.0 (или более поздней)

4. Нажмите **ОК**.

## <a name="creating-ado-objects-in-visual-basic"></a>Создание объектов ADO в Visual Basic

Чтобы создать переменную автоматизации и экземпляр объекта для этой переменной, можно использовать два метода: **Dim** или **CreateObject.**

### <a name="dim"></a>Dim

Ключевое слово **New** с **Dim** можно использовать для объявления и использования объектов ADO за один шаг:

```vb 
 
Dim conn As New ADODB.Connection 
```

Кроме того, объявление **заявления Dim** и объекты также могут быть двумя этапами:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> Не требуется явно использовать progid ADODB с заявлением **Dim,** если вы правильно ссылались на библиотеку ADO в проекте. Однако его использование гарантирует, что у вас не будет конфликтов именования с другими библиотеками.
> 
> Например, если вы включаете ссылки на ADO и DAO в одном проекте, необходимо включить квалификатор, чтобы указать объектную модель, которая будет применяться при моделировании объектов **Recordset,** как в следующем коде:  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

С помощью **метода CreateObject** объявление и создание объекта должны быть двумя дискретными этапами:

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Объекты, создание которых создается с помощью **CreateObject,** привязаны позднее, что означает, что они не имеют строгого типа и завершение командной строки отключено. Однако он позволяет пропустить ссылки на библиотеку ADO из проекта и позволяет вам сгенецировать определенные версии объектов. Например:

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Для этого также можно создать ссылку на библиотеку типов ADO версии 2.0 и создать объект.

Создание объектов с помощью метода **CreateObject** обычно медленнее, чем при использовании заявления **Dim.**

## <a name="handling-events"></a>Обработка событий

Для обработки событий ADO в Microsoft Visual Basic необходимо объявить переменную уровня модуля с помощью ключевого слова **WithEvents.** Переменная может быть объявлена только как часть модуля класса и должна быть объявлена на уровне модуля. Более подробное обсуждение обработки событий ADO см. в главе [7 "Обработка событий ADO".](chapter-7-handling-ado-events.md)

## <a name="visual-basic-examples"></a>Visual Basic примерах

В документацию ADO включено множество Visual Basic примеров. Дополнительные сведения см. в примерах кода [ADO в Microsoft Visual Basic.](ado-code-examples-in-microsoft-visual-basic.md)

