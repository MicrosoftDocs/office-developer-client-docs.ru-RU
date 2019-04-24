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
# <a name="stat-method-ado"></a><span data-ttu-id="1cfd5-102">Метод stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="1cfd5-102">Stat method (ADO)</span></span>

<span data-ttu-id="1cfd5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cfd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1cfd5-104">Получает сведения о объекте **Stream** .</span><span class="sxs-lookup"><span data-stu-id="1cfd5-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cfd5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cfd5-105">Syntax</span></span>

<span data-ttu-id="1cfd5-106">Длинный *поток*. Stat (*статстг*, *статфлаг*)</span><span class="sxs-lookup"><span data-stu-id="1cfd5-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="1cfd5-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cfd5-107">Return value</span></span>

<span data-ttu-id="1cfd5-108">Длинное значение, указывающее состояние операции.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cfd5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cfd5-109">Parameters</span></span>

|<span data-ttu-id="1cfd5-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="1cfd5-110">Parameter</span></span>|<span data-ttu-id="1cfd5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1cfd5-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1cfd5-112">*Статстг*</span><span class="sxs-lookup"><span data-stu-id="1cfd5-112">*StatStg*</span></span> |<span data-ttu-id="1cfd5-113">Структура СТАТСТГ, которая будет заполнена информацией о потоке.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-113">A STATSTG structure that will be filled in with information about the stream.</span></span> <span data-ttu-id="1cfd5-114">Реализация метода Stat, используемого объектом Stream объекта ADO, не заполняет все поля структуры.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-114">The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="1cfd5-115">*Статфлаг*</span><span class="sxs-lookup"><span data-stu-id="1cfd5-115">*StatFlag*</span></span> |<span data-ttu-id="1cfd5-116">Указывает, что этот метод не возвращает некоторые члены структуры СТАТСТГ, тем самым сохраняя операцию выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-116">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="1cfd5-117">Значения берутся из перечисления СТАТФЛАГ.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-117">Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="1cfd5-118">Перечисление СТАТФЛАГ имеет два значения:</span><span class="sxs-lookup"><span data-stu-id="1cfd5-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="1cfd5-119">— СТАТФЛАГ_ДЕФАУЛТ: 0</span><span class="sxs-lookup"><span data-stu-id="1cfd5-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="1cfd5-120">— СТАТФЛАГ_НОНАМЕ: 1</span><span class="sxs-lookup"><span data-stu-id="1cfd5-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="1cfd5-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="1cfd5-121">Remarks</span></span>

<span data-ttu-id="1cfd5-122">Версия метода Stat, реализованного для объекта Stream объекта ADO, заполняет следующие поля структуры СТАТСТГ:</span><span class="sxs-lookup"><span data-stu-id="1cfd5-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="1cfd5-123">Field</span><span class="sxs-lookup"><span data-stu-id="1cfd5-123">Field</span></span>|<span data-ttu-id="1cfd5-124">Описание</span><span class="sxs-lookup"><span data-stu-id="1cfd5-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1cfd5-125">*Пвкснаме*</span><span class="sxs-lookup"><span data-stu-id="1cfd5-125">*pwcsName*</span></span> |<span data-ttu-id="1cfd5-126">Строка, содержащая имя потока, если он доступен, а значение Статфлаг СТАТФЛАГ\_не указано.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="1cfd5-127">*Кбсизе*</span><span class="sxs-lookup"><span data-stu-id="1cfd5-127">*cbSize*</span></span> |<span data-ttu-id="1cfd5-128">Указывает размер массива байтов или потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="1cfd5-129">*мтиме*</span><span class="sxs-lookup"><span data-stu-id="1cfd5-129">*mtime*</span></span> |<span data-ttu-id="1cfd5-130">Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="1cfd5-131">*ктиме*</span><span class="sxs-lookup"><span data-stu-id="1cfd5-131">*ctime*</span></span> |<span data-ttu-id="1cfd5-132">Указывает время создания для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="1cfd5-133">*атиме*</span><span class="sxs-lookup"><span data-stu-id="1cfd5-133">*atime*</span></span> |<span data-ttu-id="1cfd5-134">Указывает время последнего доступа для этого хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="1cfd5-135">Если в\_параметре статфлаг ЗАДАНО имя статфлаг, то имя потока не возвращается.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="1cfd5-136">Если в\_параметре статфлаг не ЗАДАНО имя статфлаг, а для текущего потока нет имени, это значение будет равно E\_нотимпл.</span><span class="sxs-lookup"><span data-stu-id="1cfd5-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

