---
title: Documents Collection (DAO)
TOCTitle: Documents Collection
ms:assetid: ae2fef58-34e7-eea6-ca51-d3903432c7f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821742(v=office.15)
ms:contentKeyID: 48547063
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ed91166c8a244c20848069ecfd936a25c10accd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878166"
---
# <a name="documents-collection-dao"></a><span data-ttu-id="96b80-102">Documents Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="96b80-102">Documents Collection (DAO)</span></span>


<span data-ttu-id="96b80-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96b80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96b80-104">Коллекция **документов** содержит все объекты **документа** для определенного типа объекта (Microsoft Access базами данных, ядро только).</span><span class="sxs-lookup"><span data-stu-id="96b80-104">A **Documents** collection contains all of the **Document** objects for a specific type of object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="96b80-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="96b80-105">Remarks</span></span>

<span data-ttu-id="96b80-106">Каждый объект- **контейнер** имеет **документы** коллекцию, содержащую объекты **документов** , которые описывают экземпляры встроенные объекты типа, указанного в качестве **контейнера**.</span><span class="sxs-lookup"><span data-stu-id="96b80-106">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span>

<span data-ttu-id="96b80-107">Для ссылки на объект **Document** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="96b80-107">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="96b80-108">**Документы** (0)</span><span class="sxs-lookup"><span data-stu-id="96b80-108">**Documents**(0)</span></span>

  - <span data-ttu-id="96b80-109">**Документы** («*имя*»)</span><span class="sxs-lookup"><span data-stu-id="96b80-109">**Documents**("*name*")</span></span>

  - <span data-ttu-id="96b80-110">**Документы**\!\[*имя*\]</span><span class="sxs-lookup"><span data-stu-id="96b80-110">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="96b80-111">Пример</span><span class="sxs-lookup"><span data-stu-id="96b80-111">Example</span></span>

<span data-ttu-id="96b80-112">В этом примере создается перечисление коллекции **документов** контейнер таблиц и затем создается перечисление коллекции **свойств** первый объект **документа** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="96b80-112">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

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

