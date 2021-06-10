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

Настройка проекта ADO и написание кода ADO аналогично тому, используете ли вы Visual Basic или Visual Basic для приложений. Этот раздел адресов с помощью ADO с Visual Basic и Visual Basic для приложений и отмечает любые различия.

## <a name="referencing-the-ado-library"></a>Ссылки на библиотеку ADO

Библиотека ADO должна быть со ссылкой на ваш проект.

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>Ссылка на ADO из Microsoft Visual Basic

1. В Visual Basic, из **меню Project** выберите **Ссылки ...**.

2. Выберите **microsoft ActiveX объекты данных x.x Library** из списка. Убедитесь, что выбраны по крайней мере следующие библиотеки:
   
   - Visual Basic for Applications
   - Visual Basic и процедуры
   - Visual Basic объектов и процедур
   - Автоматизация OLE

3. Нажмите кнопку **ОК**.

Вы можете использовать ADO так же легко с Visual Basic для приложений, например с помощью Microsoft Access.

### <a name="to-reference-ado-from-microsoft-access"></a>Ссылка на ADO из Microsoft Access

1. В Microsoft Access выберите или создайте модуль из вкладки **Модули** в окне **Базы** данных.

2. Из меню **Tools** выберите **Ссылки...**.

3. Выберите **microsoft ActiveX объекты данных x.x Library** из списка. Убедитесь, что выбраны по крайней мере следующие библиотеки:
    
   - Visual Basic for Applications
   - Объектная библиотека Microsoft Access 11.0 (или более позднее)

4. Нажмите кнопку **ОК**.

## <a name="creating-ado-objects-in-visual-basic"></a>Создание объектов ADO в Visual Basic

Чтобы создать переменную автоматизации и экземпляр объекта для этой переменной, можно использовать два метода: **Dim** или **CreateObject.**

### <a name="dim"></a>Dim

Вы можете использовать ключевое слово **New** with **Dim** для объявления и мгновенного объявления объектов ADO за один шаг:

```vb 
 
Dim conn As New ADODB.Connection 
```

Кроме того,  объявление дим-заявления и моментация объектов также могут быть двумя шагами:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> Не требуется явно использовать прогид ADODB с заявлением **Dim,** если вы правильно ссылались на библиотеку ADO в проекте. Однако его использование гарантирует, что у вас не будет конфликтов именования с другими библиотеками.
> 
> Например, если вы включаете ссылки на ADO и DAO в одном проекте, необходимо включить квалификатор, чтобы указать объектную модель, которую следует использовать при моментации объектов **Recordset,** как в следующем коде:  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

С помощью **метода CreateObject** мгновенный декларирование и объект должны быть двумя дискретными шагами:

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Объекты, мгновенные с **помощью CreateObject,** связаны с опозданием, что означает, что они не сильно введите и завершение командной строки отключено. Однако это позволяет пропустить ссылки на библиотеку ADO из проекта и позволяет мгновенно использовать определенные версии объектов. Пример.

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Это также можно сделать, создав ссылку на библиотеку типов ADO версии 2.0 и создав объект.

Мгновенные объекты с помощью **метода CreateObject** обычно медленнее, чем с помощью **дим-заявления.**

## <a name="handling-events"></a>Обработка событий

Чтобы обрабатывать события ADO в Microsoft Visual Basic, необходимо объявить переменную уровня модуля с помощью ключевого слова **WithEvents.** Переменная может быть объявлена только в составе классового модуля и должна быть объявлена на уровне модуля. Более полное обсуждение обработки событий ADO см. в главе [7. Обработка событий ADO.](chapter-7-handling-ado-events.md)

## <a name="visual-basic-examples"></a>Visual Basic примеры

Многие Visual Basic включены в документацию ADO. Дополнительные сведения см. в примерах кода ADO в [Microsoft Visual Basic.](ado-code-examples-in-microsoft-visual-basic.md)

