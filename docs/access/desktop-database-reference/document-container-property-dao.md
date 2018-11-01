---
title: Document.Container Property (DAO)
TOCTitle: Container Property
ms:assetid: aa1ace1d-f0b8-e0b0-20b6-d3e296254c51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821451(v=office.15)
ms:contentKeyID: 48546940
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053320
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bc6ddd2da224c219a73318a916087b33643ef123
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891284"
---
# <a name="documentcontainer-property-dao"></a>Document.Container Property (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает имя объекта **[контейнера](container-object-dao.md)** , которому принадлежит объект **Document** (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение* . Контейнер

*выражение* Переменная, которая представляет собой объект- **документов** .

## <a name="example"></a>Пример

В этом примере отображаются свойства **контейнера** для различных объектов **документа** .

```vb 
Sub ContainerPropertyX() 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Display the container name for the first Document 
 ' object in each Container object's Documents collection. 
 For Each ctrLoop In dbsNorthwind.Containers 
 Debug.Print "Document: " & ctrLoop.Documents(0).Name 
 Debug.Print " Container = " & _ 
 ctrLoop.Documents(0).Container 
 Next ctrLoop 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

