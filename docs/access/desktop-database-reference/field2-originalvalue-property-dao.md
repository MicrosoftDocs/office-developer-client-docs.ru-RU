---
title: Field2.OriginalValue Property (DAO)
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
ms.openlocfilehash: a08612076ba138e5e181eec80bec2350fe27ec86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483015"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="b4010-102">Field2.OriginalValue Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b4010-102">Field2.OriginalValue Property (DAO)</span></span>


<span data-ttu-id="b4010-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4010-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="b4010-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4010-104">Syntax</span></span>

<span data-ttu-id="b4010-105">*выражение* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="b4010-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="b4010-106">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="b4010-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4010-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4010-107">Remarks</span></span>

<span data-ttu-id="b4010-108">Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="b4010-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="b4010-109">Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** .</span><span class="sxs-lookup"><span data-stu-id="b4010-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="b4010-110">Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт.</span><span class="sxs-lookup"><span data-stu-id="b4010-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="b4010-111">В этом случае будет доступен через свойство **VisibleValue** новое значение в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b4010-111">When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

