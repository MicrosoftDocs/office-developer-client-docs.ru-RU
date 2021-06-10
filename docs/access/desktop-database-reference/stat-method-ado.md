---
title: Метод Stat — ActiveX объектов данных (ADO)
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
# <a name="stat-method-ado"></a><span data-ttu-id="e83e6-102">Метод Stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="e83e6-102">Stat method (ADO)</span></span>

<span data-ttu-id="e83e6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e83e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e83e6-104">Извлекает сведения об **объекте Stream.**</span><span class="sxs-lookup"><span data-stu-id="e83e6-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e83e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e83e6-105">Syntax</span></span>

<span data-ttu-id="e83e6-106">Длинный *поток*. Stat (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="e83e6-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="e83e6-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e83e6-107">Return value</span></span>

<span data-ttu-id="e83e6-108">Длинное значение, указывающее состояние операции.</span><span class="sxs-lookup"><span data-stu-id="e83e6-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="e83e6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e83e6-109">Parameters</span></span>

|<span data-ttu-id="e83e6-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="e83e6-110">Parameter</span></span>|<span data-ttu-id="e83e6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e83e6-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e83e6-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="e83e6-112">*StatStg*</span></span> |<span data-ttu-id="e83e6-113">Структура STATSTG, которая будет заполнена сведениями о потоке.</span><span class="sxs-lookup"><span data-stu-id="e83e6-113">A STATSTG structure that will be filled in with information about the stream.</span></span> <span data-ttu-id="e83e6-114">Реализация метода Stat, используемого объектом ADO Stream, не заполняет все поля структуры.</span><span class="sxs-lookup"><span data-stu-id="e83e6-114">The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="e83e6-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="e83e6-115">*StatFlag*</span></span> |<span data-ttu-id="e83e6-116">Указывает, что этот метод не возвращает часть участников в структуре STATSTG, тем самым сэкономив операцию распределения памяти.</span><span class="sxs-lookup"><span data-stu-id="e83e6-116">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="e83e6-117">Значения взяты из перемерения STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="e83e6-117">Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="e83e6-118">В переумериях STATFLAG есть два значения:</span><span class="sxs-lookup"><span data-stu-id="e83e6-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="e83e6-119">- STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="e83e6-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="e83e6-120">- STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="e83e6-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="e83e6-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e83e6-121">Remarks</span></span>

<span data-ttu-id="e83e6-122">Версия метода Stat, реализованного для объекта ADO Stream, заполняется в следующих полях структуры STATSTG:</span><span class="sxs-lookup"><span data-stu-id="e83e6-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="e83e6-123">Поле</span><span class="sxs-lookup"><span data-stu-id="e83e6-123">Field</span></span>|<span data-ttu-id="e83e6-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e83e6-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e83e6-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="e83e6-125">*pwcsName*</span></span> |<span data-ttu-id="e83e6-126">Строка, содержащая имя потока, если она доступна, и значение STATFLAG NONAME не \_ указывается.</span><span class="sxs-lookup"><span data-stu-id="e83e6-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="e83e6-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="e83e6-127">*cbSize*</span></span> |<span data-ttu-id="e83e6-128">Указывает размер массива байтов или потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="e83e6-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="e83e6-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="e83e6-129">*mtime*</span></span> |<span data-ttu-id="e83e6-130">Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="e83e6-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="e83e6-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="e83e6-131">*ctime*</span></span> |<span data-ttu-id="e83e6-132">Указывает время создания для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="e83e6-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="e83e6-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="e83e6-133">*atime*</span></span> |<span data-ttu-id="e83e6-134">Указывает время последнего доступа для этого массива хранения, потока или byte.</span><span class="sxs-lookup"><span data-stu-id="e83e6-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="e83e6-135">Если в параметре \_ StatFlag указан STATFLAG NONAME, имя потока не возвращается.</span><span class="sxs-lookup"><span data-stu-id="e83e6-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="e83e6-136">Если в параметре StatFlag не указан STATFLAG NONAME, а для текущего потока нет имени, это значение будет \_ E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e83e6-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

