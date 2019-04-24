---
title: Свойство Field. Висиблевалуе (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292918"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="c22c4-102">Свойство Field. Висиблевалуе (DAO)</span><span class="sxs-lookup"><span data-stu-id="c22c4-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="c22c4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c22c4-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c22c4-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c22c4-104">Syntax</span></span>

<span data-ttu-id="c22c4-105">*Expression* . Висиблевалуе</span><span class="sxs-lookup"><span data-stu-id="c22c4-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="c22c4-106">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="c22c4-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c22c4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c22c4-107">Remarks</span></span>

<span data-ttu-id="c22c4-108">Это свойство содержит значение поля, которое в настоящее время находится в базе данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="c22c4-108">This property contains the value of the field that is currently in the database on the server.</span></span> <span data-ttu-id="c22c4-109">Во время оптимистического пакетного обновления может произойти конфликт, при котором второй клиент изменил то же поле и записывает данные между моментом, когда первый клиент получил данные, и попытка обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="c22c4-109">During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt.</span></span> <span data-ttu-id="c22c4-110">В этом случае значение, которое будет доступно во втором наборе клиентов, будет доступно через это свойство.</span><span class="sxs-lookup"><span data-stu-id="c22c4-110">When this happens, the value that the second client set will be accessible through this property.</span></span>

