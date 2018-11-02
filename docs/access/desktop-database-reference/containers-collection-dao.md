---
title: Коллекция контейнеров (DAO)
TOCTitle: Containers Object
ms:assetid: 4996ee39-ea13-f560-3069-dd7bc6022119
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193464(v=office.15)
ms:contentKeyID: 48544642
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be25a2f8b5d6da7b569858d758b3fb541cf9be51
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920440"
---
# <a name="containers-collection-dao"></a><span data-ttu-id="a236b-102">Коллекция контейнеров (DAO)</span><span class="sxs-lookup"><span data-stu-id="a236b-102">Containers collection (DAO)</span></span>

<span data-ttu-id="a236b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a236b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a236b-104">Коллекция **контейнеров** содержит все объекты **контейнера** , определенные в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a236b-104">A **Containers** collection contains all of the **Container** objects that are defined in a database.</span></span>

## <a name="remarks"></a><span data-ttu-id="a236b-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="a236b-105">Remarks</span></span>

<span data-ttu-id="a236b-106">Каждый объект **базы данных** имеет коллекцию **контейнеров** , состоящую из встроенных объектов **контейнера** .</span><span class="sxs-lookup"><span data-stu-id="a236b-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="a236b-107">Некоторые из этих объектов **контейнера** определяются ядро базы данных Microsoft Access, в то время как другие пользователи могут быть определены с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="a236b-107">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span>

## <a name="example"></a><span data-ttu-id="a236b-108">Пример</span><span class="sxs-lookup"><span data-stu-id="a236b-108">Example</span></span>

<span data-ttu-id="a236b-109">В этом примере перечисляются коллекция **контейнеров** базы данных Northwind и коллекции **свойств** для каждого объекта- **контейнера** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="a236b-109">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX()
    
       Dim dbsNorthwind As Database
       Dim ctrLoop As Container
       Dim prpLoop As Property
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
    
          ' Enumerate Containers collection.
          For Each ctrLoop In .Containers
             Debug.Print "Properties of " & ctrLoop.Name _
                & " container"
    
             ' Enumerate Properties collection of each
             ' Container object.
             For Each prpLoop In ctrLoop.Properties
                Debug.Print "  " & prpLoop.Name _
                   & " = " prpLoop
             Next prpLoop
    
          Next ctrLoop
    
          .Close
       End With
    
    End Sub
```
