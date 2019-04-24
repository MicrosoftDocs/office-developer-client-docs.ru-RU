---
title: Recordset, свойства SourceRecordset (RDS)
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
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="3f61b-102">Recordset, свойства SourceRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="3f61b-102">Recordset, SourceRecordset properties (RDS)</span></span>

<span data-ttu-id="3f61b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f61b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f61b-104">Указывает объект **Recordset** , возвращенный из настраиваемого бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="3f61b-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f61b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f61b-105">Syntax</span></span>

<span data-ttu-id="3f61b-106">*Элемент управления*. SourceRecordset = *Recordset*</span><span class="sxs-lookup"><span data-stu-id="3f61b-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="3f61b-107">\*\* = *Элемент управления*"набор данных". Recordset</span><span class="sxs-lookup"><span data-stu-id="3f61b-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="3f61b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f61b-108">Parameters</span></span>

|<span data-ttu-id="3f61b-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="3f61b-109">Parameter</span></span>|<span data-ttu-id="3f61b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3f61b-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3f61b-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3f61b-111">*DataControl*</span></span> |<span data-ttu-id="3f61b-112">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="3f61b-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="3f61b-113">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="3f61b-113">*Recordset*</span></span> |<span data-ttu-id="3f61b-114">Объектная переменная, представляющая объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="3f61b-114">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3f61b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="3f61b-115">Remarks</span></span>

<span data-ttu-id="3f61b-116">Вы можете задать для свойства **SourceRecordset** [набор записей](recordset-object-ado.md) , возвращенный из настраиваемого бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="3f61b-116">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="3f61b-117">Эти свойства позволяют приложению обрабатывать процесс привязки с помощью настраиваемого процесса.</span><span class="sxs-lookup"><span data-stu-id="3f61b-117">These properties allow an application to handle the binding process by means of a custom process.</span></span> <span data-ttu-id="3f61b-118">Они получают набор строк, заключенный в **набор записей** и позволяющий напрямую взаимодействовать с **набором записей**, выполняя такие действия, как Настройка свойств или итерация по **набору записей**.</span><span class="sxs-lookup"><span data-stu-id="3f61b-118">They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="3f61b-119">Вы можете задать свойство **SourceRecordset** или прочитать свойство **Recordset** во время выполнения в коде сценария.</span><span class="sxs-lookup"><span data-stu-id="3f61b-119">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="3f61b-120">**SourceRecordset** — это свойство, доступное только для записи, в отличие от свойства **Recordset** , которое является свойством, предназначенным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3f61b-120">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

