---
title: Свойство field2. OriginalValue (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292743"
---
# <a name="field2originalvalue-property-dao"></a><span data-ttu-id="bfbd9-102">Свойство field2. OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="bfbd9-102">Field2.OriginalValue property (DAO)</span></span>


<span data-ttu-id="bfbd9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfbd9-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="bfbd9-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfbd9-104">Syntax</span></span>

<span data-ttu-id="bfbd9-105">*Expression* . OriginalValue</span><span class="sxs-lookup"><span data-stu-id="bfbd9-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="bfbd9-106">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="bfbd9-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfbd9-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="bfbd9-107">Remarks</span></span>

<span data-ttu-id="bfbd9-108">Во время оптимистического пакетного обновления может произойти конфликт, при котором второй клиент изменяет одно и то же поле и запись между моментом, когда первый клиент получает данные, и пытается выполнить обновление первого клиента.</span><span class="sxs-lookup"><span data-stu-id="bfbd9-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="bfbd9-109">Свойство **originalValue** содержит значение поля во время последнего начала пакетного **обновления** .</span><span class="sxs-lookup"><span data-stu-id="bfbd9-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="bfbd9-110">Если это значение не отвечает фактическому значению в базе данных при попытке пакетного **обновления** выполнить запись в базу данных, происходит конфликт.</span><span class="sxs-lookup"><span data-stu-id="bfbd9-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="bfbd9-111">В этом случае новое значение в базе данных будет доступно через свойство **висиблевалуе** .</span><span class="sxs-lookup"><span data-stu-id="bfbd9-111">When this happens, the new value in the database will be accessible through the **VisibleValue** property.</span></span>

