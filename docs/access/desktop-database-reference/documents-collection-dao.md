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
# <a name="documents-collection-dao"></a><span data-ttu-id="ae700-102">Коллекция документов (DAO)</span><span class="sxs-lookup"><span data-stu-id="ae700-102">Documents collection (DAO)</span></span>


<span data-ttu-id="ae700-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae700-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae700-104">Коллекция **документов** содержит все объекты **Document** для определенного типа объекта (только базы данных базы данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ae700-104">A **Documents** collection contains all of the **Document** objects for a specific type of object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae700-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae700-105">Remarks</span></span>

<span data-ttu-id="ae700-106">Каждый **объект Контейнер** имеет коллекцию **Документов,** содержащую объекты **Document,** описывая экземпляры встроенных объектов типа, указанного **контейнером.**</span><span class="sxs-lookup"><span data-stu-id="ae700-106">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span>

<span data-ttu-id="ae700-107">Чтобы сослаться на объект **Document** в коллекции по его порядковому номеру или по параметру свойства **Name,** используйте любую из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="ae700-107">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="ae700-108">**Документы**(0)</span><span class="sxs-lookup"><span data-stu-id="ae700-108">**Documents**(0)</span></span>

  - <span data-ttu-id="ae700-109">\**Документы\*\*\*("имя")*</span><span class="sxs-lookup"><span data-stu-id="ae700-109">**Documents**("*name*")</span></span>

  - <span data-ttu-id="ae700-110"> \! Документы \[ *имя*\]</span><span class="sxs-lookup"><span data-stu-id="ae700-110">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="ae700-111">Пример</span><span class="sxs-lookup"><span data-stu-id="ae700-111">Example</span></span>

<span data-ttu-id="ae700-112">В этом примере содержится коллекция Документов контейнера Tables, а затем — коллекция **свойств** первого объекта **Document** в коллекции. </span><span class="sxs-lookup"><span data-stu-id="ae700-112">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

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

