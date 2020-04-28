---
title: Свойство field2. Висиблевалуе (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0161ea66068457b53a9667a6739c3a3a0458c8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292617"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="89d47-102">Свойство field2. Висиблевалуе (DAO)</span><span class="sxs-lookup"><span data-stu-id="89d47-102">Field2.VisibleValue property (DAO)</span></span>


<span data-ttu-id="89d47-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89d47-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="89d47-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d47-104">Syntax</span></span>

<span data-ttu-id="89d47-105">*Expression* . висиблевалуе</span><span class="sxs-lookup"><span data-stu-id="89d47-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="89d47-106">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="89d47-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d47-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="89d47-107">Remarks</span></span>

<span data-ttu-id="89d47-108">Это свойство содержит значение поля, которое в настоящее время находится в базе данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="89d47-108">This property contains the value of the field that is currently in the database on the server.</span></span> <span data-ttu-id="89d47-109">Во время оптимистического пакетного обновления может произойти конфликт, при котором второй клиент изменил то же поле и записывает данные между моментом, когда первый клиент получил данные, и попытка обновления первого клиента.</span><span class="sxs-lookup"><span data-stu-id="89d47-109">During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt.</span></span> <span data-ttu-id="89d47-110">В этом случае значение, которое будет доступно во втором наборе клиентов, будет доступно через это свойство.</span><span class="sxs-lookup"><span data-stu-id="89d47-110">When this happens, the value that the second client set will be accessible through this property.</span></span>

