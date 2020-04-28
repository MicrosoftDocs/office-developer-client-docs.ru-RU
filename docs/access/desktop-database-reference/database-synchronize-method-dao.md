---
title: Метод Database. Synchronize (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294710"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="95d01-102">Метод Database. Synchronize (DAO)</span><span class="sxs-lookup"><span data-stu-id="95d01-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="95d01-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95d01-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95d01-104">Синхронизирует две реплики.</span><span class="sxs-lookup"><span data-stu-id="95d01-104">Synchronizes two replicas.</span></span> <span data-ttu-id="95d01-105">(Только для рабочих областей Microsoft Access.)</span><span class="sxs-lookup"><span data-stu-id="95d01-105">(Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="95d01-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95d01-106">Syntax</span></span>

<span data-ttu-id="95d01-107">*Expression* . Синхронизация (***дбпаснаме***, ***ексчанжетипе***)</span><span class="sxs-lookup"><span data-stu-id="95d01-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="95d01-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="95d01-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="95d01-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="95d01-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95d01-110">Имя</span><span class="sxs-lookup"><span data-stu-id="95d01-110">Name</span></span></p></th>
<th><p><span data-ttu-id="95d01-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="95d01-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="95d01-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="95d01-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="95d01-113">Описание</span><span class="sxs-lookup"><span data-stu-id="95d01-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95d01-114"><em>дбпаснаме</em></span><span class="sxs-lookup"><span data-stu-id="95d01-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="95d01-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="95d01-115">Required</span></span></p></td>
<td><p><span data-ttu-id="95d01-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="95d01-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="95d01-117">Путь к целевой реплике, с которой будет синхронизироваться база данных.</span><span class="sxs-lookup"><span data-stu-id="95d01-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95d01-118"><em>ексчанжетипе</em></span><span class="sxs-lookup"><span data-stu-id="95d01-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="95d01-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="95d01-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="95d01-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="95d01-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="95d01-121">Константа <strong><a href="synchronizetypeenum-enumeration-dao.md">синчронизетипинум</a></strong> , указывающая направление синхронизации изменений между двумя базами данных.</span><span class="sxs-lookup"><span data-stu-id="95d01-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="95d01-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="95d01-122">Remarks</span></span>

<span data-ttu-id="95d01-123">**Синхронизация** используется для обмена данными и изменения структуры между двумя базами данных.</span><span class="sxs-lookup"><span data-stu-id="95d01-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="95d01-124">Изменения макета всегда происходят первыми.</span><span class="sxs-lookup"><span data-stu-id="95d01-124">Design changes always happen first.</span></span> <span data-ttu-id="95d01-125">Для обмена данными обе базы данных должны иметь одинаковый уровень оформления.</span><span class="sxs-lookup"><span data-stu-id="95d01-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="95d01-126">Например, Exchange типа **дбрепекспортчанжес** может привести к изменениям структуры в реплике, несмотря на то, что изменения данных проходят только из базы данных в дбпаснаме.</span><span class="sxs-lookup"><span data-stu-id="95d01-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="95d01-127">Реплика, определенная в Дбпаснаме, должна быть частью того же набора реплик.</span><span class="sxs-lookup"><span data-stu-id="95d01-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="95d01-128">Если обе реплики имеют одинаковое свойство **replicaId** или основные структуры для двух различных наборов реплик, синхронизация завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="95d01-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="95d01-129">При синхронизации двух реплик через Интернет необходимо использовать константу **дбрепсинЦинтернет** .</span><span class="sxs-lookup"><span data-stu-id="95d01-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="95d01-130">В этом случае вместо указания пути к локальной сети необходимо указать URL-адрес для аргумента Дбпаснаме.</span><span class="sxs-lookup"><span data-stu-id="95d01-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="95d01-131">Невозможно синхронизировать частичные реплики с другими частичными репликами.</span><span class="sxs-lookup"><span data-stu-id="95d01-131">You can't synchronize partial replicas with other partial replicas.</span></span> <span data-ttu-id="95d01-132">Дополнительные сведения см. в методе [популатепартиал](database-populatepartial-method-dao.md) .</span><span class="sxs-lookup"><span data-stu-id="95d01-132">See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


