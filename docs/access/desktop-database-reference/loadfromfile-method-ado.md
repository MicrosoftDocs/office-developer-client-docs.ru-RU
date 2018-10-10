---
title: LoadFromFile Method (ADO)
TOCTitle: LoadFromFile Method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a2a86e739b8744f40c481eb81b86f2f1ae5fad12
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479982"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="3b988-102">LoadFromFile Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b988-102">LoadFromFile Method (ADO)</span></span>


<span data-ttu-id="3b988-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b988-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3b988-104">Загружает содержимое существующего файла в [поток](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3b988-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b988-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b988-105">Syntax</span></span>

<span data-ttu-id="3b988-106">*Поток*. LoadFromFile *имя файла*</span><span class="sxs-lookup"><span data-stu-id="3b988-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameter"></a><span data-ttu-id="3b988-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="3b988-107">Parameter</span></span>

  - <span data-ttu-id="3b988-108">*Имя файла*</span><span class="sxs-lookup"><span data-stu-id="3b988-108">*FileName*</span></span>

  - <span data-ttu-id="3b988-109">**Строковое** значение, которое содержит имя файла для загрузки в **поток**.</span><span class="sxs-lookup"><span data-stu-id="3b988-109">A **String** value that contains the name of a file to be loaded into the **Stream**.</span></span> <span data-ttu-id="3b988-110">*Имя файла* может содержать любой допустимый путь и имя в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="3b988-110">*FileName* can contain any valid path and name in UNC format.</span></span> <span data-ttu-id="3b988-111">Если указанный файл не существует, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="3b988-111">If the specified file does not exist, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b988-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b988-112">Remarks</span></span>

<span data-ttu-id="3b988-113">Этот метод может использоваться для загрузки содержимого локального файла в объект **потока** .</span><span class="sxs-lookup"><span data-stu-id="3b988-113">This method may be used to load the contents of a local file into a **Stream** object.</span></span> <span data-ttu-id="3b988-114">Могут быть использованы для загрузки содержимого локального файла на сервер.</span><span class="sxs-lookup"><span data-stu-id="3b988-114">This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="3b988-115">Объект **Stream** должен быть уже открыт до вызова метода **LoadFromFile**.</span><span class="sxs-lookup"><span data-stu-id="3b988-115">The **Stream** object must be already open before calling **LoadFromFile**.</span></span> <span data-ttu-id="3b988-116">Этот метод не изменяет привязка объекта **потока** ; оно будет по-прежнему привязан к объектом, заданным с URL-адрес или **записи** , с которой был открыт в **поток** .</span><span class="sxs-lookup"><span data-stu-id="3b988-116">This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="3b988-117">**LoadFromFile** перезаписывает содержимое текущего объекта **потока** данные, прочитанные из файла.</span><span class="sxs-lookup"><span data-stu-id="3b988-117">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file.</span></span> <span data-ttu-id="3b988-118">Содержимое файла перезаписываются все существующие байтов **потока** .</span><span class="sxs-lookup"><span data-stu-id="3b988-118">Any existing bytes in the **Stream** are overwritten by the contents of the file.</span></span> <span data-ttu-id="3b988-119">Любые ранее существующего оставшихся байтов и выполнив [EOS](eos-property-ado.md) , созданные **LoadFromFile**усекаются.</span><span class="sxs-lookup"><span data-stu-id="3b988-119">Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="3b988-120">После вызова **LoadFromFile**, имеет значение текущей позиции в начало **потока** ([положение](position-property-ado.md) — 0).</span><span class="sxs-lookup"><span data-stu-id="3b988-120">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="3b988-121">Так как два байта могут быть добавлены в начало потока для кодирования, размер потока может отличаться размер файла, из которого был загружен.</span><span class="sxs-lookup"><span data-stu-id="3b988-121">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

