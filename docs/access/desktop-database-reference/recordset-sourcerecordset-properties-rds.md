---
title: Recordset, SourceRecordset Properties (RDS)
TOCTitle: Recordset, SourceRecordset Properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a66e803738c16d291817eb80e7f680ff9c3c71e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481263"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="37e41-102">Recordset, SourceRecordset Properties (RDS)</span><span class="sxs-lookup"><span data-stu-id="37e41-102">Recordset, SourceRecordset Properties (RDS)</span></span>


<span data-ttu-id="37e41-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37e41-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37e41-104">Указывает, возвращать пользовательский бизнес-объект объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="37e41-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37e41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37e41-105">Syntax</span></span>

<span data-ttu-id="37e41-106">*DataControl*. SourceRecordset = *набора записей*</span><span class="sxs-lookup"><span data-stu-id="37e41-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="37e41-107">*Набор записей* = *DataControl*. Набор записей</span><span class="sxs-lookup"><span data-stu-id="37e41-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="37e41-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="37e41-108">Parameters</span></span>

  - <span data-ttu-id="37e41-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="37e41-109">*DataControl*</span></span>

  - <span data-ttu-id="37e41-110">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="37e41-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="37e41-111">*Набор записей*</span><span class="sxs-lookup"><span data-stu-id="37e41-111">*Recordset*</span></span>

  - <span data-ttu-id="37e41-112">Объектная переменная, представляющий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="37e41-112">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="37e41-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="37e41-113">Remarks</span></span>

<span data-ttu-id="37e41-114">Свойства **SourceRecordset** значение [набора записей](recordset-object-ado.md) , возвращаемых настраиваемых бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="37e41-114">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="37e41-115">Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса.</span><span class="sxs-lookup"><span data-stu-id="37e41-115">These properties allow an application to handle the binding process by means of a custom process.</span></span> <span data-ttu-id="37e41-116">Они получают набор строк, заключенное в **набор записей** , чтобы вы могли взаимодействовать непосредственно с **набора записей**, для выполнения действий, таких как установка свойств или итерации **записей**.</span><span class="sxs-lookup"><span data-stu-id="37e41-116">They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="37e41-117">Можно задать свойство **SourceRecordset** или чтение свойства **набора записей** во время выполнения в код сценария.</span><span class="sxs-lookup"><span data-stu-id="37e41-117">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="37e41-118">**SourceRecordset** является свойством только для записи, в отличие от свойства **набора записей** , которое является свойством только для чтения.</span><span class="sxs-lookup"><span data-stu-id="37e41-118">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

