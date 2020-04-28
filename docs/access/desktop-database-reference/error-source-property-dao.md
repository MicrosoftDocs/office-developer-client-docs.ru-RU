---
title: Свойство Error. Source (DAO)
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
# <a name="errorsource-property-dao"></a>Свойство Error. Source (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает имя объекта или приложения, которые изначально вызвали ошибку.

## <a name="syntax"></a>Синтаксис

*Expression* . Source

*Expression (выражение* ) Переменная, представляющая объект **Error** .

## <a name="remarks"></a>Примечания

Как правило, значением свойства **Source** является имя класса объекта или программный идентификатор. Используйте свойство **Source** , чтобы предоставить пользователям сведения о том, что код не может обработать ошибку, созданную в объекте другого приложения.

Например, если вы обращаетесь к Microsoft Excel и создаете ошибку "деление на ноль", Microsoft Excel устанавливает **ошибку. Number** в код Microsoft Excel для этой ошибки и задает для свойства **Source** значение Excel. Application. Обратите внимание, что если ошибка возникает в другом объекте, вызываемом Microsoft Excel, то Microsoft Excel перехватывает ошибку, но по-прежнему задается **ошибка. Number** для кода Microsoft Excel. Однако другие свойства объекта **Error** (включая **источник**) сохранят значения, заданные в объекте, который сформировал ошибку. Свойство **Source** всегда содержит имя объекта, который изначально создал ошибку.

На основе всей документации об ошибках можно написать код, который будет обрабатывать ошибку соответствующим образом. В случае сбоя обработчика ошибок можно использовать сведения об объекте **[Error](error-object-dao.md)** , чтобы описать ошибку для пользователя, используя свойство **Source** и другие свойства **ошибки** , чтобы предоставить пользователю сведения о том, какой объект вызвал ошибку, описание ошибки и т. д.


> [!NOTE]
> Конструкция **On Error Resume Next** может быть предпочтительной при возникновении ошибок **goto** при возникновении ошибок, возникших во время доступа к другим объектам. Проверка свойства объекта **Error** после каждого взаимодействия с объектом приводит к удалению неоднозначности объекта, к которому был получен код при возникновении ошибки. Таким образом, вы можете проверить, какой объект поместил код ошибки в **Error. Number**, а также о том, какой объект создал ошибку (**Error. Source**).

## <a name="example"></a>Пример

В этом примере вызывается ошибка, выполняется ее перехват и отображаются свойства **Description**, **Number**, **Source**, **HelpContext**и **HelpFile** полученного объекта **Error** .

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
