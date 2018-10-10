---
title: Charset Property (ADO)
TOCTitle: Charset Property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84436f814bbc2a503e843d4e9832fa2bab612b58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482515"
---
# <a name="charset-property-ado"></a><span data-ttu-id="eb431-102">Charset Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="eb431-102">Charset Property (ADO)</span></span>


<span data-ttu-id="eb431-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb431-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb431-104">Указывает набор знаков, в которой содержимое текстового [потока](stream-object-ado.md) преобразования для хранения в буфере внутренних объектов потока.</span><span class="sxs-lookup"><span data-stu-id="eb431-104">Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="eb431-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="eb431-105">Settings and Return Values</span></span>

<span data-ttu-id="eb431-106">Задает или возвращает **строковое** значение, указывающее кодировку, в которой будут переведены содержимое **потока** .</span><span class="sxs-lookup"><span data-stu-id="eb431-106">Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated.</span></span> <span data-ttu-id="eb431-107">Значение по умолчанию — «Юникод».</span><span class="sxs-lookup"><span data-stu-id="eb431-107">The default value is "Unicode".</span></span> <span data-ttu-id="eb431-108">Допустимые значения типичного строк, передаваемых через интерфейс как набор строк символов Интернета (например, «iso-8859-1», «Windows-1252", и т.д.).</span><span class="sxs-lookup"><span data-stu-id="eb431-108">Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.).</span></span> <span data-ttu-id="eb431-109">Список строк набора символов, известные системы, в разделе подразделы HKEY\_КЛАССЫ\_КОРНЕВОЙ\\MIME\\базы данных\\набор символов в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="eb431-109">For a list of the character set strings that is known by a system, see the subkeys of HKEY\_CLASSES\_ROOT\\MIME\\Database\\Charset in the Windows Registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb431-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb431-110">Remarks</span></span>

<span data-ttu-id="eb431-111">В объект текстового **потока** данных текст хранится в набор знаков, указанный в свойстве **набор символов** .</span><span class="sxs-lookup"><span data-stu-id="eb431-111">In a text **Stream** object, text data is stored in the character set specified by the **Charset** property.</span></span> <span data-ttu-id="eb431-112">Значение по умолчанию — Юникод.</span><span class="sxs-lookup"><span data-stu-id="eb431-112">The default is Unicode.</span></span> <span data-ttu-id="eb431-113">Свойство **Charset** используется для преобразования данные в **поток** или выходе из **потока**.</span><span class="sxs-lookup"><span data-stu-id="eb431-113">The **Charset** property is used for converting data going into the **Stream** or coming out of the **Stream**.</span></span> <span data-ttu-id="eb431-114">К примеру Если **поток** содержит данные ISO-8859-1, данные копируются в BSTR, объект **Stream** будет преобразования данных в Юникод.</span><span class="sxs-lookup"><span data-stu-id="eb431-114">For example, if the **Stream** contains ISO-8859-1 data and that data is copied to a BSTR, the **Stream** object will convert the data to Unicode.</span></span> <span data-ttu-id="eb431-115">Обратное также имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="eb431-115">The reverse is also true.</span></span>

<span data-ttu-id="eb431-116">Для открытия **потока**текущего [положения](position-property-ado.md) значения в начале **потока** (0) должны иметь возможность задать **набор символов**.</span><span class="sxs-lookup"><span data-stu-id="eb431-116">For an open **Stream**, the current [Position](position-property-ado.md) must be at the beginning of the **Stream** (0) to be able to set **Charset**.</span></span>

<span data-ttu-id="eb431-117">**Набор символов** используется только с объектами **потока** текста ([Тип](type-property-ado-stream.md) — **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="eb431-117">**Charset** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="eb431-118">Это свойство игнорируется, если **Тип** — **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="eb431-118">This property is ignored if **Type** is **adTypeBinary**.</span></span>

