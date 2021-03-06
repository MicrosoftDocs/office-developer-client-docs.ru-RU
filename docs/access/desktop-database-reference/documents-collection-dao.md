---
title: Коллекция документов (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f6edd02c316fdff3f64b8a09c1504c46c9812a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293751"
---
# <a name="documents-collection-dao"></a>Коллекция документов (DAO)


**Область применения**: Access 2013, Office 2013

Коллекция **документов** содержит все объекты **Document** для определенного типа объекта (только базы данных базы данных Microsoft Access).

## <a name="remarks"></a>Примечания

Каждый **объект Контейнер** имеет коллекцию **Документов,** содержащую объекты **Document,** описывая экземпляры встроенных объектов типа, указанного **контейнером.**

Чтобы сослаться на объект **Document** в коллекции по его порядковому номеру или по параметру свойства **Name,** используйте любую из следующих форм синтаксиса:

  - **Документы**(0)

  - **Документы***("имя")*

  -  \! Документы \[ *имя*\]

## <a name="example"></a>Пример

В этом примере содержится коллекция Документов контейнера Tables, а затем — коллекция **свойств** первого объекта **Document** в коллекции. 

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

