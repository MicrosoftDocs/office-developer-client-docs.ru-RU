---
title: Свойства Recordset и SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307590"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="20923-102">Свойства Recordset и SourceRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="20923-102">Recordset, SourceRecordset properties (RDS)</span></span>

<span data-ttu-id="20923-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20923-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20923-104">Указывает объект **Recordset,** возвращенный из пользовательского бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="20923-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="20923-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20923-105">Syntax</span></span>

<span data-ttu-id="20923-106">*DataControl*. SourceRecordset = *Recordset*</span><span class="sxs-lookup"><span data-stu-id="20923-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="20923-107">*Recordset*  =  *DataControl*. Recordset</span><span class="sxs-lookup"><span data-stu-id="20923-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="20923-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="20923-108">Parameters</span></span>

|<span data-ttu-id="20923-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="20923-109">Parameter</span></span>|<span data-ttu-id="20923-110">Описание</span><span class="sxs-lookup"><span data-stu-id="20923-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="20923-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="20923-111">*DataControl*</span></span> |<span data-ttu-id="20923-112">Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="20923-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="20923-113">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="20923-113">*Recordset*</span></span> |<span data-ttu-id="20923-114">Объектная переменная, представляюная объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="20923-114">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="20923-115">Заметки</span><span class="sxs-lookup"><span data-stu-id="20923-115">Remarks</span></span>

<span data-ttu-id="20923-116">Можно установить для **свойства SourceRecordset** набор [записей,](recordset-object-ado.md) возвращаемый из пользовательского бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="20923-116">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="20923-117">Эти свойства позволяют приложению обрабатывать процесс привязки с помощью пользовательского процесса.</span><span class="sxs-lookup"><span data-stu-id="20923-117">These properties allow an application to handle the binding process by means of a custom process.</span></span> <span data-ttu-id="20923-118">Они получают набор строк, завернутый в набор **записей,** чтобы вы могли взаимодействовать непосредственно с **набором записей,** выполняя такие действия, как установка свойств или итерации через **recordset.**</span><span class="sxs-lookup"><span data-stu-id="20923-118">They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="20923-119">Вы можете установить свойство **SourceRecordset** или прочитать свойство **Recordset** во время запуска в коде скриптов.</span><span class="sxs-lookup"><span data-stu-id="20923-119">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="20923-120">**SourceRecordset** — это свойство только для записи, в отличие от свойства **Recordset,** которое является свойством только для чтения.</span><span class="sxs-lookup"><span data-stu-id="20923-120">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

