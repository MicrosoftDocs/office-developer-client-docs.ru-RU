---
title: IsolationLevel Property (ADO)
TOCTitle: IsolationLevel Property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7424258f4b5a69764189f33a902956f370a56094
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481574"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="62b9c-102">IsolationLevel Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="62b9c-102">IsolationLevel Property (ADO)</span></span>


<span data-ttu-id="62b9c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="62b9c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62b9c-104">Указывает уровень изоляции для объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="62b9c-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="62b9c-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="62b9c-105">Settings and Return Values</span></span>

<span data-ttu-id="62b9c-106">Задает или возвращает значение [IsolationLevelEnum](isolationlevelenum.md) .</span><span class="sxs-lookup"><span data-stu-id="62b9c-106">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value.</span></span> <span data-ttu-id="62b9c-107">Значение по умолчанию — **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="62b9c-107">The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62b9c-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="62b9c-108">Remarks</span></span>

<span data-ttu-id="62b9c-109">Используйте свойство **IsolationLevel** , чтобы установить уровень изоляции объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="62b9c-109">Use the **IsolationLevel** property to set the isolation level of a **Connection** object.</span></span> <span data-ttu-id="62b9c-110">Параметр не вступят в силу только при следующем вызове метода [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="62b9c-110">The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="62b9c-111">Если уровень изоляции, которые вы запрашиваете недоступен, поставщик может возвращать Далее больший уровень изоляции.</span><span class="sxs-lookup"><span data-stu-id="62b9c-111">If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="62b9c-112">Свойство **IsolationLevel** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="62b9c-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="62b9c-113">**Службы удаленных данных об использовании** При использовании на объект подключения со стороны клиента, свойство **IsolationLevel** можно задать только к **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="62b9c-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="62b9c-114">Так как пользователей работе с отключенных объектов **наборов записей** в кэш со стороны клиента, может быть многопользовательской проблемы.</span><span class="sxs-lookup"><span data-stu-id="62b9c-114">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues.</span></span> <span data-ttu-id="62b9c-115">Например попытку обновления одной записи двух различных пользователей удаленной службы данных просто позволяет пользователю, сначала обновляет запись «win».</span><span class="sxs-lookup"><span data-stu-id="62b9c-115">For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win."</span></span> <span data-ttu-id="62b9c-116">Запрос на обновление второго пользователя завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="62b9c-116">The second user's update request will fail with an error.</span></span>

