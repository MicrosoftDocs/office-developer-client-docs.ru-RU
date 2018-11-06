---
title: Коллекция Properties (ADO)
TOCTitle: Properties collection (ADO)
ms:assetid: 4d662790-1252-c930-e6f9-edf6a38636af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249245(v=office.15)
ms:contentKeyID: 48544729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231104
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a4e683781fc2c508b34717447fcac6f02f54d6ff
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997849"
---
# <a name="properties-collection-ado"></a><span data-ttu-id="4a582-102">Коллекция Properties (ADO)</span><span class="sxs-lookup"><span data-stu-id="4a582-102">Properties collection (ADO)</span></span>

<span data-ttu-id="4a582-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a582-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a582-104">Содержит все объекты [Свойства](property-object-ado.md) для указанного экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="4a582-104">Contains all the [Property](property-object-ado.md) objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a582-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a582-105">Remarks</span></span>

<span data-ttu-id="4a582-106">Некоторые объекты ADO имеют коллекции **свойств** , состоящих из объектов **свойств** .</span><span class="sxs-lookup"><span data-stu-id="4a582-106">Some ADO objects have a **Properties** collection made up of **Property** objects.</span></span> <span data-ttu-id="4a582-107">Каждый объект **свойство** соответствует характеристик объекта ADO поставщика.</span><span class="sxs-lookup"><span data-stu-id="4a582-107">Each **Property** object corresponds to a characteristic of the ADO object specific to the provider.</span></span>

> [!NOTE]
> <span data-ttu-id="4a582-108">В разделе [Свойства](property-object-ado.md) объекта более подробное объяснение того, как использовать **свойство** объектов.</span><span class="sxs-lookup"><span data-stu-id="4a582-108">See the [Property](property-object-ado.md) object topic for a more detailed explanation of how to use **Property** objects.</span></span>

<span data-ttu-id="4a582-109">**Динамические свойства** объекта **набора записей** выйдет из области действия (становятся недоступными) при закрытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4a582-109">The **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

