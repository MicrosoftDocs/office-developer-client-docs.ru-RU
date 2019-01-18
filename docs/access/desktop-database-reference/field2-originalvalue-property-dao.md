---
title: Свойство Field2.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e3da5f7438ae83010c6ecc109dccf5d7a8eb9ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726136"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="78652-102">Свойство Field2.OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="78652-102">Field2.OriginalValue property (DAO)</span></span>


<span data-ttu-id="78652-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78652-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="78652-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78652-104">Syntax</span></span>

<span data-ttu-id="78652-105">*выражение* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="78652-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="78652-106">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="78652-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="78652-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="78652-107">Remarks</span></span>

<span data-ttu-id="78652-108">Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="78652-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="78652-109">Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** .</span><span class="sxs-lookup"><span data-stu-id="78652-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="78652-110">Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт.</span><span class="sxs-lookup"><span data-stu-id="78652-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="78652-111">В этом случае будет доступен через свойство **VisibleValue** новое значение в базе данных.</span><span class="sxs-lookup"><span data-stu-id="78652-111">When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

