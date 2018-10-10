---
title: CopyTo Method (ADO)
TOCTitle: CopyTo Method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bd949b92068619b76ac78d5e62cde0e247ed7b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481187"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="46114-102">CopyTo Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="46114-102">CopyTo Method (ADO)</span></span>


<span data-ttu-id="46114-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46114-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="46114-104">Копирует указанного числа символов или байтов (в зависимости от [типа](type-property-ado-stream.md)) в [потоке](stream-object-ado.md) другой объект **Stream** .</span><span class="sxs-lookup"><span data-stu-id="46114-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46114-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46114-105">Syntax</span></span>

<span data-ttu-id="46114-106">*Поток*. CopyTo *DestStream*, *NumChars*</span><span class="sxs-lookup"><span data-stu-id="46114-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="46114-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="46114-107">Parameters</span></span>

  - <span data-ttu-id="46114-108">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="46114-108">*DestStream*</span></span>

  - <span data-ttu-id="46114-109">Объект значение переменной, которая содержит ссылку на объект open **потока** .</span><span class="sxs-lookup"><span data-stu-id="46114-109">An object variable value that contains a reference to an open **Stream** object.</span></span> <span data-ttu-id="46114-110">Текущего **потока** копируется в место назначения **потока** , указанного идентификатором *DestStream*.</span><span class="sxs-lookup"><span data-stu-id="46114-110">The current **Stream** is copied to the destination **Stream** specified by *DestStream*.</span></span> <span data-ttu-id="46114-111">Целевой **поток** уже должен быть открыт.</span><span class="sxs-lookup"><span data-stu-id="46114-111">The destination **Stream** must already be open.</span></span> <span data-ttu-id="46114-112">Если это не так, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="46114-112">If not, a run-time error occurs.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="46114-113">Параметр <EM>DestStream</EM> не может быть прокси-сервера объекта <STRONG>потока</STRONG> , так как это требуется доступ к частный интерфейс на объект <STRONG>Stream</STRONG> , нельзя удаленно отправить клиенту.</span><span class="sxs-lookup"><span data-stu-id="46114-113">The <EM>DestStream</EM> parameter may not be a proxy of <STRONG>Stream</STRONG> object because this requires access to a private interface on the <STRONG>Stream</STRONG> object that cannot be remoted to the client.</span></span></P>



  - <span data-ttu-id="46114-114">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="46114-114">*NumChars*</span></span>

  - <span data-ttu-id="46114-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="46114-115">Optional.</span></span> <span data-ttu-id="46114-116">**Целое число, указывающее число байтов или знаков для копирования из текущей позиции в источнике **потока** в целевой **поток**.**</span><span class="sxs-lookup"><span data-stu-id="46114-116">An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**.</span></span> <span data-ttu-id="46114-117">Значение по умолчанию — 1, что указывает, что все символы или байт копируются из текущей позиции [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="46114-117">The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46114-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="46114-118">Remarks</span></span>

<span data-ttu-id="46114-119">Этот метод копирует указанного числа символов или байтов, начиная с текущей позиции, указанного в свойстве [положение](position-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="46114-119">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property.</span></span> <span data-ttu-id="46114-120">Если указанный номер больше, чем доступно число байт до **EOS**, затем копируются только символов или байтов, начиная с текущей позиции **EOS** .</span><span class="sxs-lookup"><span data-stu-id="46114-120">If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied.</span></span> <span data-ttu-id="46114-121">Если значение *NumChars* – 1 или опущен, копируются все символы или байт, начиная с текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="46114-121">If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="46114-122">Если существуют символов или байтов в поток назначения, все содержимое точкой, где заканчивается копии остаются и не сокращается.</span><span class="sxs-lookup"><span data-stu-id="46114-122">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated.</span></span> <span data-ttu-id="46114-123">**Положение** становится байт сразу после последнего байта копируются.</span><span class="sxs-lookup"><span data-stu-id="46114-123">**Position** becomes the byte immediately following the last byte copied.</span></span> <span data-ttu-id="46114-124">Если вы хотите усечение этих байт, вызовите [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="46114-124">If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="46114-125">**CopyTo** можно использовать для копирования данных на целевой **поток** типа источника **потока** (их параметры свойства **Type** являются **adTypeText** или оба **adTypeBinary**).</span><span class="sxs-lookup"><span data-stu-id="46114-125">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**).</span></span> <span data-ttu-id="46114-126">Для объектов **потока** текста можно изменить значения свойства [Charset](charset-property-ado.md) целевой **поток** для преобразования из одного набора знаков в другой.</span><span class="sxs-lookup"><span data-stu-id="46114-126">For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another.</span></span> <span data-ttu-id="46114-127">Кроме того объекты **потока** текста можно успешно копируются в двоичные объекты **потока** , но двоичные объекты **потока** нельзя скопировать в объекты **потока** текста.</span><span class="sxs-lookup"><span data-stu-id="46114-127">Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

