---
title: Метод SaveToFile (ADO)
TOCTitle: SaveToFile Method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1fcb4a5365f431eed4ed30ca57a3418abac9e2e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875464"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="68ce7-102">Метод SaveToFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="68ce7-102">SaveToFile Method (ADO)</span></span>


<span data-ttu-id="68ce7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68ce7-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="68ce7-104">Сохраняет двоичные содержимое [потока](stream-object-ado.md) в файл.</span><span class="sxs-lookup"><span data-stu-id="68ce7-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ce7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68ce7-105">Syntax</span></span>

<span data-ttu-id="68ce7-106">*Поток*. SaveToFile*имя файла*, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="68ce7-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="68ce7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="68ce7-107">Parameters</span></span>

  - <span data-ttu-id="68ce7-108">*Имя файла*</span><span class="sxs-lookup"><span data-stu-id="68ce7-108">*FileName*</span></span>

  - <span data-ttu-id="68ce7-109">**Строковое** значение, которое содержит полное имя файла, в котором будет сохранен содержимое **потока** .</span><span class="sxs-lookup"><span data-stu-id="68ce7-109">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved.</span></span> <span data-ttu-id="68ce7-110">Поддерживается сохранение в любое допустимое локальное местоположение или любого расположения у вас есть доступ с помощью значения UNC.</span><span class="sxs-lookup"><span data-stu-id="68ce7-110">You can save to any valid local location, or any location you have access to via a UNC value.</span></span>

  - <span data-ttu-id="68ce7-111">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="68ce7-111">*SaveOptions*</span></span>

  - <span data-ttu-id="68ce7-112">[SaveOptionsEnum](saveoptionsenum.md) значение, указывающее, следует ли создавать новый файл с **SaveToFile**, если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="68ce7-112">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist.</span></span> <span data-ttu-id="68ce7-113">Значение по умолчанию — **adSaveCreateNotExists**.</span><span class="sxs-lookup"><span data-stu-id="68ce7-113">Default value is **adSaveCreateNotExists**.</span></span> <span data-ttu-id="68ce7-114">С помощью этих параметров можно указать, что, если указанный файл не существует, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="68ce7-114">With these options you can specify that an error occurs if the specified file does not exist.</span></span> <span data-ttu-id="68ce7-115">Также можно указать, что **SaveToFile** перезаписывает текущий содержимое существующего файла.</span><span class="sxs-lookup"><span data-stu-id="68ce7-115">You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>


> [!NOTE]
> <P><span data-ttu-id="68ce7-116">При перезаписи существующего файла (если установлено <STRONG>adSaveCreateOverwrite</STRONG> ) <STRONG>SaveToFile</STRONG> ограничивает длину любой байтов из исходного существующий файл, следующие новые <A href="eos-property-ado.md">EOS</A>.</span><span class="sxs-lookup"><span data-stu-id="68ce7-116">If you overwrite an existing file (when <STRONG>adSaveCreateOverwrite</STRONG> is set), <STRONG>SaveToFile</STRONG> truncates any bytes from the original existing file that follow the new <A href="eos-property-ado.md">EOS</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="68ce7-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="68ce7-117">Remarks</span></span>

<span data-ttu-id="68ce7-118">**SaveToFile** могут быть использованы для копирования содержимого объекта **потока** в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="68ce7-118">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file.</span></span> <span data-ttu-id="68ce7-119">Нет никаких изменений в содержимое или свойства объекта **потока** .</span><span class="sxs-lookup"><span data-stu-id="68ce7-119">There is no change in the contents or properties of the **Stream** object.</span></span> <span data-ttu-id="68ce7-120">Прежде чем вызывать **SaveToFile**объект **Stream** необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="68ce7-120">The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="68ce7-121">Этот метод не изменяет сопоставления на объект **Stream** ее базовому источнику.</span><span class="sxs-lookup"><span data-stu-id="68ce7-121">This method does not change the association of the **Stream** object to its underlying source.</span></span> <span data-ttu-id="68ce7-122">По-прежнему будет связан с исходный URL-адрес или **запись** , которая была источника при открытии объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="68ce7-122">The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="68ce7-123">После выполнения операции **SaveToFile** текущей позиции ([положение](position-property-ado.md)) в потоке задано значение начала потока (0).</span><span class="sxs-lookup"><span data-stu-id="68ce7-123">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>

