---
title: Метод LoadFromFile (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9316bc4302a559fa44082a0576595707157e9d64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289887"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="e7993-102">Метод LoadFromFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="e7993-102">LoadFromFile method (ADO)</span></span>

<span data-ttu-id="e7993-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7993-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7993-104">ЗаГружает содержимое существующего файла в [поток](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e7993-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7993-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7993-105">Syntax</span></span>

<span data-ttu-id="e7993-106">*Stream*. *Имя файла* LoadFromFile</span><span class="sxs-lookup"><span data-stu-id="e7993-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="e7993-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7993-107">Parameters</span></span>

|<span data-ttu-id="e7993-108">Имя</span><span class="sxs-lookup"><span data-stu-id="e7993-108">Name</span></span> |<span data-ttu-id="e7993-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e7993-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="e7993-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="e7993-110">*FileName*</span></span> |<span data-ttu-id="e7993-111">**Строковое** значение, содержащее имя файла, который необходимо загрузить в **поток**.</span><span class="sxs-lookup"><span data-stu-id="e7993-111">A **String** value that contains the name of a file to be loaded into the **Stream**.</span></span> <span data-ttu-id="e7993-112">*Filename* может содержать любой допустимый путь и имя в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="e7993-112">*FileName* can contain any valid path and name in UNC format.</span></span> <span data-ttu-id="e7993-113">Если указанный файл не существует, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e7993-113">If the specified file does not exist, a run-time error occurs.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e7993-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7993-114">Remarks</span></span>

<span data-ttu-id="e7993-115">Этот метод можно использовать для загрузки содержимого локального файла в объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="e7993-115">This method may be used to load the contents of a local file into a **Stream** object.</span></span> <span data-ttu-id="e7993-116">Это можно использовать для отправки содержимого локального файла на сервер.</span><span class="sxs-lookup"><span data-stu-id="e7993-116">This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="e7993-117">Перед вызовом **LoadFromFile**объект **Stream** должен быть уже открыт.</span><span class="sxs-lookup"><span data-stu-id="e7993-117">The **Stream** object must be already open before calling **LoadFromFile**.</span></span> <span data-ttu-id="e7993-118">Этот метод не изменяет привязку объекта **Stream** ; Он по-прежнему будет привязан к объекту, указанному в URL-АДРЕСе или **записи** , с которой был изначально открыт **поток** .</span><span class="sxs-lookup"><span data-stu-id="e7993-118">This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="e7993-119">**LoadFromFile** перезаписывает текущее содержимое объекта **Stream** , используя данные, считанные из файла.</span><span class="sxs-lookup"><span data-stu-id="e7993-119">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file.</span></span> <span data-ttu-id="e7993-120">Все существующие в потоке \*\*\*\* байты перезаписываются содержимым файла.</span><span class="sxs-lookup"><span data-stu-id="e7993-120">Any existing bytes in the **Stream** are overwritten by the contents of the file.</span></span> <span data-ttu-id="e7993-121">Все ранее существующие и оставшиеся байты после [EOS](eos-property-ado.md) , созданного с помощью **LoadFromFile**, усекаются.</span><span class="sxs-lookup"><span data-stu-id="e7993-121">Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="e7993-122">После вызова **LoadFromFile**текущее положение устанавливается равным началу **потока** ([позиция](position-property-ado.md) равна 0).</span><span class="sxs-lookup"><span data-stu-id="e7993-122">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="e7993-123">Так как в начало потока можно добавить 2 байта для кодирования, размер потока может не совпадать с размером файла, из которого он был загружен.</span><span class="sxs-lookup"><span data-stu-id="e7993-123">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

