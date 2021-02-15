---
title: Метод SaveToFile (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f3b08c9df435c7ce995a40af7b8ad5466b79245d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308927"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="ef573-102">Метод SaveToFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="ef573-102">SaveToFile method (ADO)</span></span>

<span data-ttu-id="ef573-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef573-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef573-104">Сохраняет двоичное содержимое [Stream](stream-object-ado.md) в файл.</span><span class="sxs-lookup"><span data-stu-id="ef573-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef573-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef573-105">Syntax</span></span>

<span data-ttu-id="ef573-106">*Stream*. SaveToFile *FileName*, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="ef573-106">*Stream*.SaveToFile *FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="ef573-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef573-107">Parameters</span></span>

|<span data-ttu-id="ef573-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="ef573-108">Parameter</span></span>|<span data-ttu-id="ef573-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ef573-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ef573-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="ef573-110">*FileName*</span></span> |<span data-ttu-id="ef573-111">**Строка,** содержаная полное имя файла, в котором будет сохранено содержимое **stream.**</span><span class="sxs-lookup"><span data-stu-id="ef573-111">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved.</span></span> <span data-ttu-id="ef573-112">Вы можете сохранить его в любом допустимом локальном расположении или любом расположении, к который у вас есть доступ, с помощью ЗНАЧЕНИЯ UNC.</span><span class="sxs-lookup"><span data-stu-id="ef573-112">You can save to any valid local location, or any location you have access to via a UNC value.</span></span>|
|<span data-ttu-id="ef573-113">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="ef573-113">*SaveOptions*</span></span> |<span data-ttu-id="ef573-114">Значение [SaveOptionsEnum,](saveoptionsenum.md) которое указывает, следует ли создать новый файл с помощью **SaveToFile,** если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="ef573-114">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist.</span></span> <span data-ttu-id="ef573-115">Значение по **умолчанию— adSaveCreateNotExists.**</span><span class="sxs-lookup"><span data-stu-id="ef573-115">Default value is **adSaveCreateNotExists**.</span></span> <span data-ttu-id="ef573-116">С помощью этих параметров можно указать, что ошибка возникает, если указанный файл не существует.</span><span class="sxs-lookup"><span data-stu-id="ef573-116">With these options you can specify that an error occurs if the specified file does not exist.</span></span> <span data-ttu-id="ef573-117">Можно также указать, **что SaveToFile** переописает текущее содержимое существующего файла.</span><span class="sxs-lookup"><span data-stu-id="ef573-117">You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>|

> [!NOTE]
> <span data-ttu-id="ef573-118">При перезаписи существующего файла (если **установлено adSaveCreateOverwrite),** **SaveToFile** укоревает все bytes из исходного существующего файла, который следует за новой [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ef573-118">If you overwrite an existing file (when **adSaveCreateOverwrite** is set), **SaveToFile** truncates any bytes from the original existing file that follow the new [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef573-119">Заметки</span><span class="sxs-lookup"><span data-stu-id="ef573-119">Remarks</span></span>

<span data-ttu-id="ef573-120">**SaveToFile** можно использовать для копирования содержимого объекта **Stream** в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="ef573-120">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file.</span></span> <span data-ttu-id="ef573-121">Содержимое или свойства объекта **Stream** не изменяются.</span><span class="sxs-lookup"><span data-stu-id="ef573-121">There is no change in the contents or properties of the **Stream** object.</span></span> <span data-ttu-id="ef573-122">Объект **Stream** должен быть открыт перед вызовом **SaveToFile.**</span><span class="sxs-lookup"><span data-stu-id="ef573-122">The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="ef573-123">Этот метод не меняет связь объекта **Stream** с его исходным источником.</span><span class="sxs-lookup"><span data-stu-id="ef573-123">This method does not change the association of the **Stream** object to its underlying source.</span></span> <span data-ttu-id="ef573-124">Объект **Stream** по-прежнему будет связан с исходным URL-адресом **или** записью, которая была его источником при открытом.</span><span class="sxs-lookup"><span data-stu-id="ef573-124">The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="ef573-125">После операции **SaveToFile** текущее положение [(позиция)](position-property-ado.md)в потоке устанавливается в начале потока (0).</span><span class="sxs-lookup"><span data-stu-id="ef573-125">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>

