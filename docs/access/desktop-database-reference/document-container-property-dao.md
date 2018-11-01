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
# <a name="documentcontainer-property-dao"></a><span data-ttu-id="c0e72-102">Document.Container Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0e72-102">Document.Container Property (DAO)</span></span>


<span data-ttu-id="c0e72-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0e72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0e72-104">Возвращает имя объекта **[контейнера](container-object-dao.md)** , которому принадлежит объект **Document** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c0e72-104">Returns the name of the **[Container](container-object-dao.md)** object to which a **Document** object belongs (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c0e72-105">.</span><span class="sxs-lookup"><span data-stu-id="c0e72-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="c0e72-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0e72-106">Syntax</span></span>

<span data-ttu-id="c0e72-107">*выражение* . Контейнер</span><span class="sxs-lookup"><span data-stu-id="c0e72-107">*expression* .Container</span></span>

<span data-ttu-id="c0e72-108">*выражение* Переменная, которая представляет собой объект- **документов** .</span><span class="sxs-lookup"><span data-stu-id="c0e72-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="example"></a><span data-ttu-id="c0e72-109">Пример</span><span class="sxs-lookup"><span data-stu-id="c0e72-109">Example</span></span>

<span data-ttu-id="c0e72-110">В этом примере отображаются свойства **контейнера** для различных объектов **документа** .</span><span class="sxs-lookup"><span data-stu-id="c0e72-110">This example displays the **Container** property for a variety of **Document** objects.</span></span>

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

