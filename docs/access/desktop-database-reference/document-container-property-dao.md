---
title: Свойство Document. Container (DAO)
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
localization_priority: Normal
ms.openlocfilehash: af1a531e57aaca7d497f3f71d6c16e8ea1bab177
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293828"
---
# <a name="documentcontainer-property-dao"></a><span data-ttu-id="2a3b2-102">Свойство Document. Container (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a3b2-102">Document.Container property (DAO)</span></span>


<span data-ttu-id="2a3b2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a3b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a3b2-104">Возвращает имя объекта **[контейнера](container-object-dao.md)** , к которому принадлежит объект **Document** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2a3b2-104">Returns the name of the **[Container](container-object-dao.md)** object to which a **Document** object belongs (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2a3b2-105">.</span><span class="sxs-lookup"><span data-stu-id="2a3b2-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="2a3b2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a3b2-106">Syntax</span></span>

<span data-ttu-id="2a3b2-107">*Expression* . Container</span><span class="sxs-lookup"><span data-stu-id="2a3b2-107">*expression* .Container</span></span>

<span data-ttu-id="2a3b2-108">*Expression (выражение* ) Переменная, представляющая объект **Document** .</span><span class="sxs-lookup"><span data-stu-id="2a3b2-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="example"></a><span data-ttu-id="2a3b2-109">Пример</span><span class="sxs-lookup"><span data-stu-id="2a3b2-109">Example</span></span>

<span data-ttu-id="2a3b2-110">В этом примере отображается свойство **Container** для различных объектов **Document** .</span><span class="sxs-lookup"><span data-stu-id="2a3b2-110">This example displays the **Container** property for a variety of **Document** objects.</span></span>

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

