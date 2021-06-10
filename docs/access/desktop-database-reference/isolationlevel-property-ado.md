---
title: Свойство IsolationLevel (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291151"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="e14bc-102">Свойство IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="e14bc-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="e14bc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e14bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e14bc-104">Указывает уровень изоляции для объекта [Подключения.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="e14bc-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e14bc-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="e14bc-105">Settings and return values</span></span>

<span data-ttu-id="e14bc-106">Задает или возвращает значение [IsolationLevelEnum.](isolationlevelenum.md)</span><span class="sxs-lookup"><span data-stu-id="e14bc-106">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value.</span></span> <span data-ttu-id="e14bc-107">По умолчанию **это adXactChaos.**</span><span class="sxs-lookup"><span data-stu-id="e14bc-107">The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e14bc-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="e14bc-108">Remarks</span></span>

<span data-ttu-id="e14bc-109">Используйте свойство **IsolationLevel,** чтобы установить уровень изоляции объекта **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="e14bc-109">Use the **IsolationLevel** property to set the isolation level of a **Connection** object.</span></span> <span data-ttu-id="e14bc-110">Параметр не вступает в силу до следующего вызова метода [BeginTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="e14bc-110">The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="e14bc-111">Если запрашиваемый уровень изоляции недоступен, поставщик может вернуть следующий более высокий уровень изоляции.</span><span class="sxs-lookup"><span data-stu-id="e14bc-111">If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="e14bc-112">Свойство **IsolationLevel** — это чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="e14bc-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="e14bc-113">**Удаленное использование службы данных** При этом свойство **IsolationLevel** может быть задавано только **adXactUnspecified.**</span><span class="sxs-lookup"><span data-stu-id="e14bc-113">**Remote Data Service Usage** When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="e14bc-114">Поскольку пользователи работают с отключенными объектами **Recordset** в клиентском кэше, могут возникнуть проблемы с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="e14bc-114">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues.</span></span> <span data-ttu-id="e14bc-115">Например, когда два разных пользователя пытаются обновить ту же запись, служба удаленных данных просто позволяет пользователю, который сначала обновляет запись, "выиграть".</span><span class="sxs-lookup"><span data-stu-id="e14bc-115">For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win."</span></span> <span data-ttu-id="e14bc-116">Второй запрос обновления пользователя не будет работать с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e14bc-116">The second user's update request will fail with an error.</span></span>

