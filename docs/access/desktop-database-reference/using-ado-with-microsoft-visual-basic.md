---
title: Using ADO with Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa1f9a3c7601601a1ce48ea3912a4f759d436e4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483123"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Using ADO with Microsoft Visual Basic


**Применимо к**: Access 2013 | Office 2013

Подготовка проекта ADO и написания кода ADO аналогичен использование Visual Basic или Visual Basic для приложений. Этот раздел описывает использование ADO в Visual Basic и Visual Basic для приложений и заметки о все различия.

## <a name="referencing-the-ado-library"></a>Создание ссылок на библиотеку ADO

Должна быть указана библиотека ADO файлов проекта.

**Для ссылки ADO из Microsoft Visual Basic**

1.  В Visual Basic в меню **проект** выберите **ссылки...**.

2.  Выберите в списке **Microsoft ActiveX Data Objects x.x библиотеки** . Убедитесь, что по крайней мере следующие библиотеки также выбраны:
    
    - Visual Basic для приложений
    
    - Объекты среды выполнения Visual Basic и процедуры
    
    - Visual Basic объекты и процедуры
    
    - OLE-автоматизации

3.  Нажмите кнопку **ОК**.

Можно использовать ADO так же легко, с помощью Visual Basic для приложений, например с помощью Microsoft Access.

**Для ссылки ADO из Microsoft Access**

1.  В Microsoft Access выберите или создайте модуль из вкладки **модулей** в окне **базы данных** .

2.  В меню **Сервис** выберите пункт **ссылки...**.

3.  Выберите в списке **Microsoft ActiveX Data Objects x.x библиотеки** . Убедитесь, что по крайней мере следующие библиотеки также выбраны:
    
    - Visual Basic для приложений
    
    - Библиотека объектов Microsoft Access 11.0 (или более поздней версии)

4.  Нажмите кнопку **ОК**.

## <a name="creating-ado-objects-in-visual-basic"></a>Создание объектов ADO в Visual Basic

Чтобы создать переменную автоматизации и экземпляр объекта для этой переменной, можно использовать два метода: **Dim** или **CreateObject**.

## <a name="dim"></a>Dim

Можно использовать ключевое слово **New** с **Dim** для объявите и создайте объекты ADO в один шаг:

```vb 
 
Dim conn As New ADODB.Connection 
```

Кроме того **Dim** оператор объявления и создания экземпляра объекта также может быть два действия:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```


> [!NOTE]
> <P>Не требуется явно использовать ADODB progid с помощью оператора <STRONG>Dim</STRONG> , при условии, что правильно ссылка на библиотеку ADO в проекте. Тем не менее с его помощью гарантирует, что не будут иметь конфликтов с другими библиотеками имен.</P>



Например справочные материалы, которые ADO и DAO включается в одном проекте, необходимо включить квалификатор, чтобы указать, какие объектной модели для использования при создании объектов **наборов записей** , как показано в следующем примере кода:  
Dim adoRS как ADODB. Набор записей  
  
Dim daoRS как DAO. Набор записей

## <a name="createobject"></a>Функция CreateObject

С помощью **CreateObject** метод, объявления и создания экземпляра объекта должно быть два отдельных действий:

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Объекты с **CreateObject** экземпляр позднего связывания, что означает, что они не являются строго типизированным и отключается командной строки завершения. Тем не менее он позволяет пропустить ссылки на библиотеку ADO из проекта и позволяет создавать экземпляры определенных версий объектов. Пример:

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Может также этого, а именно создание ссылки на библиотеку ADO версии 2.0 тип и создания объекта.

Создание экземпляров объектов с помощью метода **CreateObject** обычно более медленными, чем с помощью оператора **Dim** .

## <a name="handling-events"></a>Обработка событий

Для обработки событий ADO в Microsoft Visual Basic, необходимо объявить переменную уровня модуля, с помощью ключевое слово **WithEvents** . Переменная может быть объявлен только как часть модуль класса и должны быть объявлены на уровне модуля. Более подробные сведения об обработке событий ADO, в разделе [Глава 7: обработка событий ADO](chapter-7-handling-ado-events.md).

## <a name="visual-basic-examples"></a>Примеры Visual Basic

Многие примеры Visual Basic включены в документации по ADO. Для получения дополнительных сведений см [ADO в Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).

