---
title: Метод stat — объекты данных ActiveX (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308553"
---
# <a name="stat-method-ado"></a><span data-ttu-id="f3711-102">Метод stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="f3711-102">Stat method (ADO)</span></span>

<span data-ttu-id="f3711-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3711-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3711-104">Получает сведения о объекте **Stream** .</span><span class="sxs-lookup"><span data-stu-id="f3711-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3711-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3711-105">Syntax</span></span>

<span data-ttu-id="f3711-106">Длинный *поток*. Stat (*статстг*, *статфлаг*)</span><span class="sxs-lookup"><span data-stu-id="f3711-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="f3711-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3711-107">Return value</span></span>

<span data-ttu-id="f3711-108">Длинное значение, указывающее состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f3711-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3711-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3711-109">Parameters</span></span>

|<span data-ttu-id="f3711-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="f3711-110">Parameter</span></span>|<span data-ttu-id="f3711-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f3711-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f3711-112">*статстг*</span><span class="sxs-lookup"><span data-stu-id="f3711-112">*StatStg*</span></span> |<span data-ttu-id="f3711-113">Структура СТАТСТГ, которая будет заполнена информацией о потоке.</span><span class="sxs-lookup"><span data-stu-id="f3711-113">A STATSTG structure that will be filled in with information about the stream.</span></span> <span data-ttu-id="f3711-114">Реализация метода Stat, используемого объектом Stream объекта ADO, не заполняет все поля структуры.</span><span class="sxs-lookup"><span data-stu-id="f3711-114">The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="f3711-115">*статфлаг*</span><span class="sxs-lookup"><span data-stu-id="f3711-115">*StatFlag*</span></span> |<span data-ttu-id="f3711-116">Указывает, что этот метод не возвращает некоторые члены структуры СТАТСТГ, тем самым сохраняя операцию выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="f3711-116">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="f3711-117">Значения берутся из перечисления СТАТФЛАГ.</span><span class="sxs-lookup"><span data-stu-id="f3711-117">Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="f3711-118">Перечисление СТАТФЛАГ имеет два значения:</span><span class="sxs-lookup"><span data-stu-id="f3711-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="f3711-119">— STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="f3711-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="f3711-120">— STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="f3711-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="f3711-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3711-121">Remarks</span></span>

<span data-ttu-id="f3711-122">Версия метода Stat, реализованного для объекта Stream объекта ADO, заполняет следующие поля структуры СТАТСТГ:</span><span class="sxs-lookup"><span data-stu-id="f3711-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="f3711-123">Поле</span><span class="sxs-lookup"><span data-stu-id="f3711-123">Field</span></span>|<span data-ttu-id="f3711-124">Описание</span><span class="sxs-lookup"><span data-stu-id="f3711-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f3711-125">*пвкснаме*</span><span class="sxs-lookup"><span data-stu-id="f3711-125">*pwcsName*</span></span> |<span data-ttu-id="f3711-126">Строка, содержащая имя потока, если он доступен, а значение Статфлаг СТАТФЛАГ\_не указано.</span><span class="sxs-lookup"><span data-stu-id="f3711-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="f3711-127">*кбсизе*</span><span class="sxs-lookup"><span data-stu-id="f3711-127">*cbSize*</span></span> |<span data-ttu-id="f3711-128">Указывает размер массива байтов или потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="f3711-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="f3711-129">*мтиме*</span><span class="sxs-lookup"><span data-stu-id="f3711-129">*mtime*</span></span> |<span data-ttu-id="f3711-130">Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="f3711-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="f3711-131">*ктиме*</span><span class="sxs-lookup"><span data-stu-id="f3711-131">*ctime*</span></span> |<span data-ttu-id="f3711-132">Указывает время создания для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="f3711-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="f3711-133">*атиме*</span><span class="sxs-lookup"><span data-stu-id="f3711-133">*atime*</span></span> |<span data-ttu-id="f3711-134">Указывает время последнего доступа для этого хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="f3711-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="f3711-135">Если в\_параметре статфлаг ЗАДАНО имя статфлаг, то имя потока не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f3711-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="f3711-136">Если в\_параметре статфлаг не ЗАДАНО имя статфлаг, а для текущего потока нет имени, это значение будет равно E\_нотимпл.</span><span class="sxs-lookup"><span data-stu-id="f3711-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

