---
title: Свойство Error.Source (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 79c5fa1e01bbb6bce4f2cef705f23f3259bf0678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293443"
---
# <a name="errorsource-property-dao"></a>Свойство Error.Source (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает имя объекта или приложения, которые изначально создали ошибку.

## <a name="syntax"></a>Синтаксис

*выражение .* Source

*выражение* Переменная, представляюная объект **Error.**

## <a name="remarks"></a>Заметки

Значение **свойства Source** обычно является именем класса объекта или программным кодом. Используйте свойство **Source,** чтобы предоставить пользователям информацию, когда код не может обработать ошибку, созданную в объекте в другом приложении.

Например, если при доступе к Microsoft Excel создается ошибка "Деление на ноль", Microsoft Excel задает **error.Number** в коде Microsoft Excel для этой ошибки и задает для свойства **Source** значение Excel.Application. Обратите внимание, что если ошибка создается в другом объекте, который называется Microsoft Excel, Microsoft Excel перехватывает ошибку и по-прежнему задает **Error.Number** в коде Microsoft Excel. Однако другие свойства **объекта Error** (включая **Source)** сохраняют значения, установленные объектом, который создал ошибку. Свойство **Source** всегда содержит имя объекта, который изначально вызвал ошибку.

На основе всей документации по ошибкам можно написать код, который будет обрабатывать ошибку соответствующим образом. Если обработитель ошибок не удается, можно использовать сведения об объекте **[Error,](error-object-dao.md)** чтобы описать ошибку для пользователя, используя свойство **Source** и другие свойства **Error,** чтобы предоставить пользователю сведения о том, какой объект изначально вызвал ошибку, описание ошибки и так далее.


> [!NOTE]
> Конструкция **On Error Resume Next** может быть предпочтительнее, чем On Error **GoTo** при работе с ошибками, созданными при доступе к другим объектам. Проверка свойства **объекта Error** после каждого взаимодействия с объектом устраняет неоднозначность того, к каков объект, к которому был доступ код при ошибке. Таким образом, вы можете быть уверены, какой объект поместил код ошибки в **Error.Number,** а также какой объект изначально вызвал ошибку (**Error.Source).**

## <a name="example"></a>Пример

В этом примере показана приодерживая ошибка, она застигает ее и отображает свойства **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов **Error.**

```vb
    Sub DescriptionX() 
     
     Dim dbsTest As Database 
     
     On Error GoTo ErrorHandler 
     
     ' Intentionally trigger an error. 
     Set dbsTest = OpenDatabase("NoDatabase") 
     
     Exit Sub 
     
    ErrorHandler: 
     Dim strError As String 
     Dim errLoop As Error 
     
     ' Enumerate Errors collection and display properties of 
     ' each Error object. 
     For Each errLoop In Errors 
     With errLoop 
     strError = _ 
     "Error #" & .Number & vbCr 
     strError = strError & _ 
     " " & .Description & vbCr 
     strError = strError & _ 
     " (Source: " & .Source & ")" & vbCr 
     strError = strError & _ 
     "Press F1 to see topic " & .HelpContext & vbCr 
     strError = strError & _ 
     " in the file " & .HelpFile & "." 
     End With 
     MsgBox strError 
     Next 
     
     Resume Next 
     
    End Sub
```
