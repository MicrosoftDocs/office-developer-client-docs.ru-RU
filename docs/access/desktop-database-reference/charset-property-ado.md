---
title: Свойство Charset (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca4640940c217fd81cac4ba1d8ffaf769b506fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296390"
---
# <a name="charset-property-ado"></a><span data-ttu-id="45b78-102">Свойство Charset (ADO)</span><span class="sxs-lookup"><span data-stu-id="45b78-102">Charset property (ADO)</span></span>


<span data-ttu-id="45b78-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45b78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45b78-104">Указывает набор символов, в который необходимо [](stream-object-ado.md) перевести содержимое текстового потока для хранения в внутреннем буфере объектов Stream.</span><span class="sxs-lookup"><span data-stu-id="45b78-104">Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="45b78-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="45b78-105">Settings and return values</span></span>

<span data-ttu-id="45b78-106">Задает или возвращает **значение String,** которое указывает набор символов,  в который будет переведено содержимое потока.</span><span class="sxs-lookup"><span data-stu-id="45b78-106">Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated.</span></span> <span data-ttu-id="45b78-107">Значение по умолчанию — "Unicode".</span><span class="sxs-lookup"><span data-stu-id="45b78-107">The default value is "Unicode".</span></span> <span data-ttu-id="45b78-108">Допустимые значения — это типичные строки, переданные интерфейсу в качестве строк набора символов Интернета (например, "iso-8859-1", "Windows-1252" и т.д.).</span><span class="sxs-lookup"><span data-stu-id="45b78-108">Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.).</span></span> <span data-ttu-id="45b78-109">Список строк набора символов, известных системе, см. в подкайке базы данных HKEY \_ CLASSES \_ ROOT \\ MIME \\ в Windows \\ Реестре.</span><span class="sxs-lookup"><span data-stu-id="45b78-109">For a list of the character set strings that is known by a system, see the subkeys of HKEY\_CLASSES\_ROOT\\MIME\\Database\\Charset in the Windows Registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b78-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="45b78-110">Remarks</span></span>

<span data-ttu-id="45b78-111">В объекте **text Stream** текстовые данные хранятся в наборе символов, заданном **свойством Charset.**</span><span class="sxs-lookup"><span data-stu-id="45b78-111">In a text **Stream** object, text data is stored in the character set specified by the **Charset** property.</span></span> <span data-ttu-id="45b78-112">По умолчанию — Юникод.</span><span class="sxs-lookup"><span data-stu-id="45b78-112">The default is Unicode.</span></span> <span data-ttu-id="45b78-113">Свойство **Charset** используется для преобразования данных, вступающих в **поток** или вылетеющих из **потока.**</span><span class="sxs-lookup"><span data-stu-id="45b78-113">The **Charset** property is used for converting data going into the **Stream** or coming out of the **Stream**.</span></span> <span data-ttu-id="45b78-114">Например, если  поток содержит данные ISO-8859-1 и эти данные копируются в BSTR, объект **Stream** преобразует данные в Unicode.</span><span class="sxs-lookup"><span data-stu-id="45b78-114">For example, if the **Stream** contains ISO-8859-1 data and that data is copied to a BSTR, the **Stream** object will convert the data to Unicode.</span></span> <span data-ttu-id="45b78-115">Обратное также верно.</span><span class="sxs-lookup"><span data-stu-id="45b78-115">The reverse is also true.</span></span>

<span data-ttu-id="45b78-116">Для открытого **потока** текущая [позиция](position-property-ado.md) должна быть в начале потока (0), чтобы иметь возможность установить **Charset**. </span><span class="sxs-lookup"><span data-stu-id="45b78-116">For an open **Stream**, the current [Position](position-property-ado.md) must be at the beginning of the **Stream** (0) to be able to set **Charset**.</span></span>

<span data-ttu-id="45b78-117">**Charset** используется только с текстовыми **объектами Stream** [(Type](type-property-ado-stream.md) **is adTypeText).**</span><span class="sxs-lookup"><span data-stu-id="45b78-117">**Charset** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="45b78-118">Это свойство игнорируется, **если Type** **является adTypeBinary.**</span><span class="sxs-lookup"><span data-stu-id="45b78-118">This property is ignored if **Type** is **adTypeBinary**.</span></span>

