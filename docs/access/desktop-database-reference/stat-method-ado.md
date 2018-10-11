---
title: Метод stat - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d2b8c69df8caba93f693194573d057d52dffeb8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480231"
---
# <a name="stat-method-ado"></a><span data-ttu-id="70d4f-102">Stat Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="70d4f-102">Stat Method (ADO)</span></span>


<span data-ttu-id="70d4f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="70d4f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="70d4f-104">Извлекает сведения о объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="70d4f-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d4f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70d4f-105">Syntax</span></span>

<span data-ttu-id="70d4f-106">Длинные *потока*. Статистика (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="70d4f-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="70d4f-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70d4f-107">Return Value</span></span>

<span data-ttu-id="70d4f-108">Значение типа long, указывающее состояние операции.</span><span class="sxs-lookup"><span data-stu-id="70d4f-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="70d4f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="70d4f-109">Parameters</span></span>

  - <span data-ttu-id="70d4f-110">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="70d4f-110">*StatStg*</span></span>

  - <span data-ttu-id="70d4f-111">Структура STATSTG, будут заполнены сведения о потоке.</span><span class="sxs-lookup"><span data-stu-id="70d4f-111">A STATSTG structure that will be filled in with information about the stream.</span></span> <span data-ttu-id="70d4f-112">Реализация метода Stat объект ADO Stream не заполните все поля структуры.</span><span class="sxs-lookup"><span data-stu-id="70d4f-112">The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>

  - <span data-ttu-id="70d4f-113">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="70d4f-113">*StatFlag*</span></span>

  - <span data-ttu-id="70d4f-114">Указывает, что этот метод не возвращает некоторые элементы в структуре STATSTG сэкономить операция выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="70d4f-114">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="70d4f-115">Значения берутся из перечисления STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="70d4f-115">Values are taken from the STATFLAG enumeration.</span></span>  
      
    <span data-ttu-id="70d4f-116">Перечисление STATFLAG имеет два значения</span><span class="sxs-lookup"><span data-stu-id="70d4f-116">The STATFLAG enumeration has two values</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="70d4f-117">Константа</span><span class="sxs-lookup"><span data-stu-id="70d4f-117">Constant</span></span></p></th>
    <th><p><span data-ttu-id="70d4f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="70d4f-118">Value</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="70d4f-119">STATFLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="70d4f-119">STATFLAG_DEFAULT</span></span></p></td>
    <td><p><span data-ttu-id="70d4f-120">0</span><span class="sxs-lookup"><span data-stu-id="70d4f-120">0</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="70d4f-121">STATFLAG_NONAME</span><span class="sxs-lookup"><span data-stu-id="70d4f-121">STATFLAG_NONAME</span></span></p></td>
    <td><p><span data-ttu-id="70d4f-122">1</span><span class="sxs-lookup"><span data-stu-id="70d4f-122">1</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="70d4f-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="70d4f-123">Remarks</span></span>

<span data-ttu-id="70d4f-124">В следующих полях структуры STATSTG заполняет версии Stat метода, реализованного в объекте ADO Stream:</span><span class="sxs-lookup"><span data-stu-id="70d4f-124">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

  - <span data-ttu-id="70d4f-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="70d4f-125">*pwcsName*</span></span>

  - <span data-ttu-id="70d4f-126">Строка, содержащая имя потока, если он доступен и StatFlag значение STATFLAG\_NONAME не указан.</span><span class="sxs-lookup"><span data-stu-id="70d4f-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>

  - <span data-ttu-id="70d4f-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="70d4f-127">*cbSize*</span></span>

  - <span data-ttu-id="70d4f-128">Указывает размер массива байтов или потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="70d4f-128">Specifies the size in bytes of the stream or byte array.</span></span>

  - <span data-ttu-id="70d4f-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="70d4f-129">*mtime*</span></span>

  - <span data-ttu-id="70d4f-130">Указывает время последнего изменения для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="70d4f-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="70d4f-131">*CTime*</span><span class="sxs-lookup"><span data-stu-id="70d4f-131">*ctime*</span></span>

  - <span data-ttu-id="70d4f-132">Указывает время создания для данного объекта хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="70d4f-132">Indicates the creation time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="70d4f-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="70d4f-133">*atime*</span></span>

  - <span data-ttu-id="70d4f-134">Указывает время последнего обращения к этой хранилища, потока или массива байтов.</span><span class="sxs-lookup"><span data-stu-id="70d4f-134">Indicates the last access time for this storage, stream or byte array.</span></span>

<span data-ttu-id="70d4f-135">Если STATFLAG\_NONAME указан в параметре StatFlag, имя потока не возвращается.</span><span class="sxs-lookup"><span data-stu-id="70d4f-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="70d4f-136">Если STATFLAG\_NONAME не указан в параметре StatFlag и нет имя не для текущего потока, это значение будет E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="70d4f-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

