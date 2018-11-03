---
title: Свойства Recordset и SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f842ad1498e0f6752299cd3d16d8c558042a850e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945784"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="bc0d7-102">Свойства Recordset и SourceRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="bc0d7-102">Recordset, SourceRecordset properties (RDS)</span></span>


<span data-ttu-id="bc0d7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc0d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc0d7-104">Указывает, возвращать пользовательский бизнес-объект объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="bc0d7-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc0d7-105">Syntax</span></span>

<span data-ttu-id="bc0d7-106">*DataControl*. SourceRecordset = *набора записей*</span><span class="sxs-lookup"><span data-stu-id="bc0d7-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="bc0d7-107">*Набор записей* = *DataControl*. Набор записей</span><span class="sxs-lookup"><span data-stu-id="bc0d7-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="bc0d7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc0d7-108">Parameters</span></span>

- <span data-ttu-id="bc0d7-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="bc0d7-109">*DataControl*</span></span>

  - <span data-ttu-id="bc0d7-110">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="bc0d7-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

- <span data-ttu-id="bc0d7-111">*Набор записей*</span><span class="sxs-lookup"><span data-stu-id="bc0d7-111">*Recordset*</span></span>

  - <span data-ttu-id="bc0d7-112">Объектная переменная, представляющий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="bc0d7-112">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc0d7-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc0d7-113">Remarks</span></span>

<span data-ttu-id="bc0d7-114">Свойства **SourceRecordset** значение [набора записей](recordset-object-ado.md) , возвращаемых настраиваемых бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="bc0d7-114">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="bc0d7-115">Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса.</span><span class="sxs-lookup"><span data-stu-id="bc0d7-115">These properties allow an application to handle the binding process by means of a custom process.</span></span> <span data-ttu-id="bc0d7-116">Они получают набор строк, заключенное в **набор записей** , чтобы вы могли взаимодействовать непосредственно с **набора записей**, для выполнения действий, таких как установка свойств или итерации **записей**.</span><span class="sxs-lookup"><span data-stu-id="bc0d7-116">They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="bc0d7-117">Можно задать свойство **SourceRecordset** или чтение свойства **набора записей** во время выполнения в код сценария.</span><span class="sxs-lookup"><span data-stu-id="bc0d7-117">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="bc0d7-118">**SourceRecordset** является свойством только для записи, в отличие от свойства **набора записей** , которое является свойством только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bc0d7-118">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

