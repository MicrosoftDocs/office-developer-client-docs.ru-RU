---
title: Перечисление LockTypeEnum (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c2d355e2a16df632d6952802914c1f921b5e9719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289859"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="2132d-102">Перечисление LockTypeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="2132d-102">LockTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="2132d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2132d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2132d-104">Указывает тип блокировки записи, используемой при открытии набора записей.</span><span class="sxs-lookup"><span data-stu-id="2132d-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2132d-105">Имя</span><span class="sxs-lookup"><span data-stu-id="2132d-105">Name</span></span></p></th>
<th><p><span data-ttu-id="2132d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="2132d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2132d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2132d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2132d-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="2132d-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="2132d-109">3</span><span class="sxs-lookup"><span data-stu-id="2132d-109">3.</span></span></p></td>
<td><p><span data-ttu-id="2132d-110">Оптимистичный параллелизм на основе идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="2132d-110">Optimistic concurrency based on record ID.</span></span> <span data-ttu-id="2132d-111">Курсор сравнивает идентификатор записи в старой и новой записях и определяет, были ли внесены изменения с момента последнего доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="2132d-111">Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2132d-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="2132d-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="2132d-113">5</span><span class="sxs-lookup"><span data-stu-id="2132d-113">5.</span></span></p></td>
<td><p><span data-ttu-id="2132d-114">Позволяет выполнять пакетные оптимистичные обновления (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="2132d-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2132d-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="2132d-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="2132d-116">1</span><span class="sxs-lookup"><span data-stu-id="2132d-116">-1</span></span></p></td>
<td><p><span data-ttu-id="2132d-117">Оптимистичный параллелизм на основе значений записей.</span><span class="sxs-lookup"><span data-stu-id="2132d-117">Optimistic concurrency based on record values.</span></span> <span data-ttu-id="2132d-118">Курсор сравнивает значения данных в старой и новой записях и определяет, были ли внесены изменения с момента последнего доступа к записи (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="2132d-118">Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <span data-ttu-id="2132d-119">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2132d-119">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2132d-120">Если вам необходим доступ ко внешним источникам данных без использования ядра СУБД Microsoft Access, воспользуйтесь объектами ADO.</span><span class="sxs-lookup"><span data-stu-id="2132d-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2132d-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="2132d-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="2132d-122">2</span><span class="sxs-lookup"><span data-stu-id="2132d-122">2.</span></span></p></td>
<td><p><span data-ttu-id="2132d-123">Пессимистичный параллелизм.</span><span class="sxs-lookup"><span data-stu-id="2132d-123">Pessimistic concurrency.</span></span> <span data-ttu-id="2132d-124">Курсор использует минимальный уровень блокировки, достаточный для гарантированного обновления записи.</span><span class="sxs-lookup"><span data-stu-id="2132d-124">Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

