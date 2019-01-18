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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698871"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="21cfd-102">Свойство IsolationLevel (ADO)</span><span class="sxs-lookup"><span data-stu-id="21cfd-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="21cfd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21cfd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21cfd-104">Указывает уровень изоляции для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="21cfd-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="21cfd-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="21cfd-105">Settings and return values</span></span>

<span data-ttu-id="21cfd-106">Задает или возвращает значение [IsolationLevelEnum](isolationlevelenum.md) .</span><span class="sxs-lookup"><span data-stu-id="21cfd-106">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value.</span></span> <span data-ttu-id="21cfd-107">Значение по умолчанию — **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="21cfd-107">The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="21cfd-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="21cfd-108">Remarks</span></span>

<span data-ttu-id="21cfd-109">Используйте свойство **IsolationLevel** , чтобы установить уровень изоляции объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="21cfd-109">Use the **IsolationLevel** property to set the isolation level of a **Connection** object.</span></span> <span data-ttu-id="21cfd-110">Параметр не вступят в силу только при следующем вызове метода [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="21cfd-110">The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="21cfd-111">Если уровень изоляции, которые вы запрашиваете недоступен, поставщик может возвращать Далее больший уровень изоляции.</span><span class="sxs-lookup"><span data-stu-id="21cfd-111">If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="21cfd-112">Свойство **IsolationLevel** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="21cfd-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="21cfd-113">**Службы удаленных данных об использовании** При использовании на объект подключения со стороны клиента, свойство **IsolationLevel** можно задать только к **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="21cfd-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="21cfd-114">Так как пользователей работе с отключенных объектов **наборов записей** в кэш со стороны клиента, может быть многопользовательской проблемы.</span><span class="sxs-lookup"><span data-stu-id="21cfd-114">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues.</span></span> <span data-ttu-id="21cfd-115">Например попытку обновления одной записи двух различных пользователей удаленной службы данных просто позволяет пользователю, сначала обновляет запись «win».</span><span class="sxs-lookup"><span data-stu-id="21cfd-115">For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win."</span></span> <span data-ttu-id="21cfd-116">Запрос на обновление второго пользователя завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="21cfd-116">The second user's update request will fail with an error.</span></span>

