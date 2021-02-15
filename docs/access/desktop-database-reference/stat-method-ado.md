---
title: Метод Stat — ActiveX Data Objects (ADO)
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
# <a name="stat-method-ado"></a><span data-ttu-id="179bd-102">Метод Stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="179bd-102">Stat method (ADO)</span></span>

<span data-ttu-id="179bd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="179bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="179bd-104">Извлекает сведения об **объекте Stream.**</span><span class="sxs-lookup"><span data-stu-id="179bd-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="179bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="179bd-105">Syntax</span></span>

<span data-ttu-id="179bd-106">Длинный *поток.* Stat(*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="179bd-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="179bd-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="179bd-107">Return value</span></span>

<span data-ttu-id="179bd-108">Длинное значение, указывающее состояние операции.</span><span class="sxs-lookup"><span data-stu-id="179bd-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="179bd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="179bd-109">Parameters</span></span>

|<span data-ttu-id="179bd-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="179bd-110">Parameter</span></span>|<span data-ttu-id="179bd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="179bd-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="179bd-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="179bd-112">*StatStg*</span></span> |<span data-ttu-id="179bd-113">Структура STATSTG, которая будет заполнена сведениями о потоке.</span><span class="sxs-lookup"><span data-stu-id="179bd-113">A STATSTG structure that will be filled in with information about the stream.</span></span> <span data-ttu-id="179bd-114">Реализация метода Stat, используемого объектом ADO Stream, не заполняет все поля структуры.</span><span class="sxs-lookup"><span data-stu-id="179bd-114">The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="179bd-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="179bd-115">*StatFlag*</span></span> |<span data-ttu-id="179bd-116">Указывает, что этот метод не возвращает некоторые члены в структуре STATSTG, тем самым экономя операцию выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="179bd-116">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="179bd-117">Значения принимаются из enumeration STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="179bd-117">Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="179bd-118">В значении STATFLAG есть два значения:</span><span class="sxs-lookup"><span data-stu-id="179bd-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="179bd-119">- STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="179bd-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="179bd-120">- STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="179bd-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="179bd-121">Заметки</span><span class="sxs-lookup"><span data-stu-id="179bd-121">Remarks</span></span>

<span data-ttu-id="179bd-122">Версия метода Stat, реализованного для объекта ADO Stream, заполняется в следующих полях структуры STATSTG:</span><span class="sxs-lookup"><span data-stu-id="179bd-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="179bd-123">Поле</span><span class="sxs-lookup"><span data-stu-id="179bd-123">Field</span></span>|<span data-ttu-id="179bd-124">Описание</span><span class="sxs-lookup"><span data-stu-id="179bd-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="179bd-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="179bd-125">*pwcsName*</span></span> |<span data-ttu-id="179bd-126">Строка, содержащая имя потока, если он доступен и значение StatFlag STATFLAG \_ NONAME не указано.</span><span class="sxs-lookup"><span data-stu-id="179bd-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="179bd-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="179bd-127">*cbSize*</span></span> |<span data-ttu-id="179bd-128">Указывает размер массива байтов или потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="179bd-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="179bd-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="179bd-129">*mtime*</span></span> |<span data-ttu-id="179bd-130">Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="179bd-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="179bd-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="179bd-131">*ctime*</span></span> |<span data-ttu-id="179bd-132">Указывает время создания для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="179bd-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="179bd-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="179bd-133">*atime*</span></span> |<span data-ttu-id="179bd-134">Указывает время последнего доступа к этому хранилищу, потоку или массиву byte.</span><span class="sxs-lookup"><span data-stu-id="179bd-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="179bd-135">Если параметр STATFLAG NONAME указан в параметре \_ StatFlag, имя потока не возвращается.</span><span class="sxs-lookup"><span data-stu-id="179bd-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="179bd-136">Если параметр STATFLAG NONAME не указан в параметре StatFlag и имя для текущего потока не доступно, это значение будет \_ иметь значение E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="179bd-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

