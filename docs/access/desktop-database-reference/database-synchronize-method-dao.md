---
title: Метод Database.Synchronize (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 65611960044ea62e42be1ea9d6c6a54d5d42d5a8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949770"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="9a6ab-102">Метод Database.Synchronize (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a6ab-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="9a6ab-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a6ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a6ab-104">Синхронизирует две реплики.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-104">Synchronizes two replicas.</span></span> <span data-ttu-id="9a6ab-105">(Microsoft Access рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="9a6ab-105">(Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a6ab-106">Syntax</span></span>

<span data-ttu-id="9a6ab-107">*выражение* . Синхронизация (***DbPathName***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="9a6ab-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="9a6ab-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="9a6ab-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a6ab-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a6ab-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a6ab-110">Имя</span><span class="sxs-lookup"><span data-stu-id="9a6ab-110">Name</span></span></p></th>
<th><p><span data-ttu-id="9a6ab-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="9a6ab-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="9a6ab-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9a6ab-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="9a6ab-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9a6ab-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a6ab-114"><em>DbPathName</em></span><span class="sxs-lookup"><span data-stu-id="9a6ab-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="9a6ab-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9a6ab-115">Required</span></span></p></td>
<td><p><span data-ttu-id="9a6ab-116"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="9a6ab-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9a6ab-117">Путь к целевой реплики, с которой синхронизируется базы данных.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a6ab-118"><em>ExchangeType</em></span><span class="sxs-lookup"><span data-stu-id="9a6ab-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="9a6ab-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="9a6ab-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="9a6ab-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9a6ab-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9a6ab-121">Константа <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> , которое указывает направление, чтобы синхронизировать изменения между двумя базами данных.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9a6ab-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a6ab-122">Remarks</span></span>

<span data-ttu-id="9a6ab-123">**Синхронизация** использовать для обмена данными и разработки изменения между двумя базами данных.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="9a6ab-124">Изменение структуры всегда выполнять сначала.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-124">Design changes always happen first.</span></span> <span data-ttu-id="9a6ab-125">Обе базы данных должны быть на том же уровне структуры при обмене данными.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="9a6ab-126">Например обмен тип **dbRepExportChanges** может привести к изменения структуры в реплике несмотря на то, что изменения данных передаются только из базы данных для DbPathName.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="9a6ab-127">Реплики, определенный в DbPathName необходимо быть членом один и тот же набор реплики.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="9a6ab-128">Если оба реплик иметь такое же значение свойства **ReplicaID** или реплик для двух различных наборов реплик, происходит сбой синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="9a6ab-129">При синхронизации двух реплик через Интернет, необходимо использовать **dbRepSyncInternet** константу.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="9a6ab-130">В этом случае укажите на универсальный код ресурса по URL-адрес для аргумента DbPathName вместо указания пути локальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="9a6ab-131">Синхронизация частичных реплик с других частичных реплик.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-131">You can't synchronize partial replicas with other partial replicas.</span></span> <span data-ttu-id="9a6ab-132">Метод [PopulatePartial](database-populatepartial-method-dao.md) для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="9a6ab-132">See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


