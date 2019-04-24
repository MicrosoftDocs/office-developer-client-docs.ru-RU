---
title: Ксактаттрибутинум (Справочник по базам данных Access на компьютере)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302571"
---
# <a name="xactattributeenum"></a><span data-ttu-id="fa1a4-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="fa1a4-102">XactAttributeEnum</span></span>

<span data-ttu-id="fa1a4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa1a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa1a4-104">Задает атрибуты транзакции для объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="fa1a4-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa1a4-105">Константа</span><span class="sxs-lookup"><span data-stu-id="fa1a4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fa1a4-106">Значение</span><span class="sxs-lookup"><span data-stu-id="fa1a4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fa1a4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fa1a4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa1a4-108"><strong>Адксактабортретаининг</strong></span><span class="sxs-lookup"><span data-stu-id="fa1a4-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="fa1a4-109">262144</span><span class="sxs-lookup"><span data-stu-id="fa1a4-109">262144</span></span></p></td>
<td><p><span data-ttu-id="fa1a4-110">Выполняет сохранение аварийных завершений; то есть при вызове <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> автоматически запускается новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="fa1a4-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="fa1a4-111">Не все поставщики поддерживают эту возможность.</span><span class="sxs-lookup"><span data-stu-id="fa1a4-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa1a4-112"><strong>Адксакткоммитретаининг</strong></span><span class="sxs-lookup"><span data-stu-id="fa1a4-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="fa1a4-113">131072</span><span class="sxs-lookup"><span data-stu-id="fa1a4-113">131072</span></span></p></td>
<td><p><span data-ttu-id="fa1a4-114">Сохраняет фиксации; то есть при вызове <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> автоматически запускается новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="fa1a4-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="fa1a4-115">Не все поставщики поддерживают эту возможность.</span><span class="sxs-lookup"><span data-stu-id="fa1a4-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fa1a4-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="fa1a4-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="fa1a4-117">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="fa1a4-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa1a4-118">Константа</span><span class="sxs-lookup"><span data-stu-id="fa1a4-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa1a4-119">Адоенумс. Ксактаттрибуте. АБОРТРЕТАИНИНГ</span><span class="sxs-lookup"><span data-stu-id="fa1a4-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa1a4-120">Адоенумс. Ксактаттрибуте. КОММИТРЕТАИНИНГ</span><span class="sxs-lookup"><span data-stu-id="fa1a4-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

