---
title: Метод stat - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc4ff8076ec07d065ba932ef0e0017edb97e703
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606957"
---
# <a name="stat-method-ado"></a><span data-ttu-id="f3f4f-102">Stat Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="f3f4f-102">Stat Method (ADO)</span></span>


<span data-ttu-id="f3f4f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3f4f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f3f4f-104">Извлекает сведения о объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="f3f4f-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f4f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3f4f-105">Syntax</span></span>

<span data-ttu-id="f3f4f-106">Длинные *потока*. Статистика (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="f3f4f-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

<span data-ttu-id="f3f4f-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f3f4f-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="f3f4f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3f4f-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="f3f4f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3f4f-109">Return value</span></span>
>>>>>>> <span data-ttu-id="f3f4f-110">master</span><span class="sxs-lookup"><span data-stu-id="f3f4f-110">master</span></span>

<span data-ttu-id="f3f4f-111">Значение типа long, указывающее состояние операции.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-111">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3f4f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3f4f-112">Parameters</span></span>

  - <span data-ttu-id="f3f4f-113">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="f3f4f-113">*StatStg*</span></span>

  - <span data-ttu-id="f3f4f-114">Структура STATSTG, будут заполнены сведения о потоке.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-114">A STATSTG structure that will be filled in with information about the stream.</span></span> <span data-ttu-id="f3f4f-115">Реализация метода Stat объект ADO Stream не заполните все поля структуры.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-115">The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>

  - <span data-ttu-id="f3f4f-116">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="f3f4f-116">*StatFlag*</span></span>

  - <span data-ttu-id="f3f4f-117">Указывает, что этот метод не возвращает некоторые элементы в структуре STATSTG сэкономить операция выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-117">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="f3f4f-118">Значения берутся из перечисления STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-118">Values are taken from the STATFLAG enumeration.</span></span>  
      
    <span data-ttu-id="f3f4f-119">Перечисление STATFLAG имеет два значения</span><span class="sxs-lookup"><span data-stu-id="f3f4f-119">The STATFLAG enumeration has two values</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="f3f4f-120">Константа</span><span class="sxs-lookup"><span data-stu-id="f3f4f-120">Constant</span></span></p></th>
    <th><p><span data-ttu-id="f3f4f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f3f4f-121">Value</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="f3f4f-122">STATFLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f3f4f-122">STATFLAG_DEFAULT</span></span></p></td>
    <td><p><span data-ttu-id="f3f4f-123">0</span><span class="sxs-lookup"><span data-stu-id="f3f4f-123">0</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f3f4f-124">STATFLAG_NONAME</span><span class="sxs-lookup"><span data-stu-id="f3f4f-124">STATFLAG_NONAME</span></span></p></td>
    <td><p><span data-ttu-id="f3f4f-125">1</span><span class="sxs-lookup"><span data-stu-id="f3f4f-125">1</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="f3f4f-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3f4f-126">Remarks</span></span>

<span data-ttu-id="f3f4f-127">В следующих полях структуры STATSTG заполняет версии Stat метода, реализованного в объекте ADO Stream:</span><span class="sxs-lookup"><span data-stu-id="f3f4f-127">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

  - <span data-ttu-id="f3f4f-128">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="f3f4f-128">*pwcsName*</span></span>

  - <span data-ttu-id="f3f4f-129">Строка, содержащая имя потока, если он доступен и StatFlag значение STATFLAG\_NONAME не указан.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-129">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>

  - <span data-ttu-id="f3f4f-130">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="f3f4f-130">*cbSize*</span></span>

  - <span data-ttu-id="f3f4f-131">Указывает размер массива байтов или потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-131">Specifies the size in bytes of the stream or byte array.</span></span>

  - <span data-ttu-id="f3f4f-132">*mtime*</span><span class="sxs-lookup"><span data-stu-id="f3f4f-132">*mtime*</span></span>

  - <span data-ttu-id="f3f4f-133">Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-133">Indicates the last modification time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="f3f4f-134">*CTime*</span><span class="sxs-lookup"><span data-stu-id="f3f4f-134">*ctime*</span></span>

  - <span data-ttu-id="f3f4f-135">Указывает время создания для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-135">Indicates the creation time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="f3f4f-136">*atime*</span><span class="sxs-lookup"><span data-stu-id="f3f4f-136">*atime*</span></span>

  - <span data-ttu-id="f3f4f-137">Указывает время последнего обращения к этой хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-137">Indicates the last access time for this storage, stream or byte array.</span></span>

<span data-ttu-id="f3f4f-138">Если STATFLAG\_NONAME указан в параметре StatFlag, имя потока не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-138">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="f3f4f-139">Если STATFLAG\_NONAME не указан в параметре StatFlag и нет имя не для текущего потока, это значение будет E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f3f4f-139">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

