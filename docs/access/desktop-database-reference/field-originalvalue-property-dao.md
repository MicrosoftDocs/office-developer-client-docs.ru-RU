---
title: Свойство Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293002"
---
# <a name="fieldoriginalvalue-property-dao"></a><span data-ttu-id="9013c-102">Свойство Field.OriginalValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="9013c-102">Field.OriginalValue property (DAO)</span></span>


<span data-ttu-id="9013c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9013c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9013c-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9013c-104">Syntax</span></span>

<span data-ttu-id="9013c-105">*выражение .* OriginalValue</span><span class="sxs-lookup"><span data-stu-id="9013c-105">*expression* .OriginalValue</span></span>

<span data-ttu-id="9013c-106">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="9013c-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9013c-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="9013c-107">Remarks</span></span>

<span data-ttu-id="9013c-108">Во время оптимистичного пакетного обновления может возникнуть конфликт, в котором второй клиент изменяет одно и то же поле и запись между моментом, когда первый клиент получает данные, и первой попыткой обновления клиента.</span><span class="sxs-lookup"><span data-stu-id="9013c-108">During an optimistic batch update, a collision may occur where a second client modifies the same field and record in between the time the first client retrieves the data and the first client's update attempt.</span></span> <span data-ttu-id="9013c-109">Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления.**</span><span class="sxs-lookup"><span data-stu-id="9013c-109">The **OriginalValue** property contains the value of the field at the time the last batch **Update** began.</span></span> <span data-ttu-id="9013c-110">Если это значение не совпадает со значением  в базе данных при попытке пакетного обновления записать в базу данных, возникает конфликт.</span><span class="sxs-lookup"><span data-stu-id="9013c-110">If this value does not match the value actually in the database when the batch **Update** attempts to write to the database, a collision occurs.</span></span> <span data-ttu-id="9013c-111">В этом случае новое значение в базе данных будет доступно через свойство **[VisibleValue.](field-visiblevalue-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="9013c-111">When this happens, the new value in the database will be accessible through the **[VisibleValue](field-visiblevalue-property-dao.md)** property.</span></span>

