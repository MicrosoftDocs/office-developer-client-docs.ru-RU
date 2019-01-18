---
title: Метод stat - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721075"
---
# <a name="stat-method-ado"></a><span data-ttu-id="aaeb4-102">Метод Stat (ADO)</span><span class="sxs-lookup"><span data-stu-id="aaeb4-102">Stat method (ADO)</span></span>

<span data-ttu-id="aaeb4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aaeb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aaeb4-104">Извлекает сведения о объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="aaeb4-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaeb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaeb4-105">Syntax</span></span>

<span data-ttu-id="aaeb4-106">Длинные *потока*. Статистика (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="aaeb4-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="aaeb4-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aaeb4-107">Return value</span></span>

<span data-ttu-id="aaeb4-108">Значение типа long, указывающее состояние операции.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="aaeb4-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="aaeb4-109">Parameters</span></span>

|<span data-ttu-id="aaeb4-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="aaeb4-110">Parameter</span></span>|<span data-ttu-id="aaeb4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="aaeb4-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="aaeb4-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="aaeb4-112">*StatStg*</span></span> |<span data-ttu-id="aaeb4-113">Структура STATSTG, будут заполнены сведения о потоке.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-113">A STATSTG structure that will be filled in with information about the stream.</span></span> <span data-ttu-id="aaeb4-114">Реализация метода Stat объект ADO Stream не заполните все поля структуры.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-114">The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="aaeb4-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="aaeb4-115">*StatFlag*</span></span> |<span data-ttu-id="aaeb4-116">Указывает, что этот метод не возвращает некоторые элементы в структуре STATSTG сэкономить операция выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-116">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="aaeb4-117">Значения берутся из перечисления STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-117">Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="aaeb4-118">Перечисление STATFLAG имеет два значения:</span><span class="sxs-lookup"><span data-stu-id="aaeb4-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="aaeb4-119">-STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="aaeb4-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="aaeb4-120">-STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="aaeb4-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="aaeb4-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="aaeb4-121">Remarks</span></span>

<span data-ttu-id="aaeb4-122">В следующих полях структуры STATSTG заполняет версии Stat метода, реализованного в объекте ADO Stream:</span><span class="sxs-lookup"><span data-stu-id="aaeb4-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="aaeb4-123">Поле</span><span class="sxs-lookup"><span data-stu-id="aaeb4-123">Field</span></span>|<span data-ttu-id="aaeb4-124">Описание</span><span class="sxs-lookup"><span data-stu-id="aaeb4-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="aaeb4-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="aaeb4-125">*pwcsName*</span></span> |<span data-ttu-id="aaeb4-126">Строка, содержащая имя потока, если он доступен и StatFlag значение STATFLAG\_NONAME не указан.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="aaeb4-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="aaeb4-127">*cbSize*</span></span> |<span data-ttu-id="aaeb4-128">Указывает размер массива байтов или потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="aaeb4-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="aaeb4-129">*mtime*</span></span> |<span data-ttu-id="aaeb4-130">Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="aaeb4-131">*CTime*</span><span class="sxs-lookup"><span data-stu-id="aaeb4-131">*ctime*</span></span> |<span data-ttu-id="aaeb4-132">Указывает время создания для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="aaeb4-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="aaeb4-133">*atime*</span></span> |<span data-ttu-id="aaeb4-134">Указывает время последнего обращения к этой хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="aaeb4-135">Если STATFLAG\_NONAME указан в параметре StatFlag, имя потока не возвращается.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="aaeb4-136">Если STATFLAG\_NONAME не указан в параметре StatFlag и нет имя не для текущего потока, это значение будет E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="aaeb4-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

