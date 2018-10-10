---
title: LockTypeEnum Enumeration (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 82a09db7baff93ba7fd51de593bc4d1dfff41dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481316"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="df835-102">LockTypeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="df835-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="df835-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="df835-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="df835-104">Указывает тип записи блокировки, используемый при открытии набора записей.</span><span class="sxs-lookup"><span data-stu-id="df835-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df835-105">Имя</span><span class="sxs-lookup"><span data-stu-id="df835-105">Name</span></span></p></th>
<th><p><span data-ttu-id="df835-106">Значение</span><span class="sxs-lookup"><span data-stu-id="df835-106">Value</span></span></p></th>
<th><p><span data-ttu-id="df835-107">Описание</span><span class="sxs-lookup"><span data-stu-id="df835-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df835-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="df835-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="df835-109">3</span><span class="sxs-lookup"><span data-stu-id="df835-109">3</span></span></p></td>
<td><p><span data-ttu-id="df835-110">Оптимистичный параллелизм на основе идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="df835-110">Optimistic concurrency based on record ID.</span></span> <span data-ttu-id="df835-111">Курсор сравнивает идентификатор записи в старых и новых записей для определения, если изменения были внесены с момента последнего обращения к записи.</span><span class="sxs-lookup"><span data-stu-id="df835-111">Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df835-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="df835-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="df835-113">5</span><span class="sxs-lookup"><span data-stu-id="df835-113">5</span></span></p></td>
<td><p><span data-ttu-id="df835-114">Позволяет производить пакетную оптимистичный обновлений (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="df835-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df835-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="df835-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="df835-116">1</span><span class="sxs-lookup"><span data-stu-id="df835-116">1</span></span></p></td>
<td><p><span data-ttu-id="df835-117">Оптимистичный параллелизм на основании значения записей.</span><span class="sxs-lookup"><span data-stu-id="df835-117">Optimistic concurrency based on record values.</span></span> <span data-ttu-id="df835-118">Курсор сравнивает значения данных в старой и новой записи, чтобы определить, если изменения были внесены момента записи последнего к которому предоставляется доступ (технология ODBCDirect рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="df835-118">Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="df835-119">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="df835-119">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="df835-120">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="df835-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df835-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="df835-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="df835-122">2</span><span class="sxs-lookup"><span data-stu-id="df835-122">2</span></span></p></td>
<td><p><span data-ttu-id="df835-123">Жесткой одновременно.</span><span class="sxs-lookup"><span data-stu-id="df835-123">Pessimistic concurrency.</span></span> <span data-ttu-id="df835-124">Курсор использует самый низкий уровень блокировки достаточными для обеспечения можно обновить запись.</span><span class="sxs-lookup"><span data-stu-id="df835-124">Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

