---
title: Свойство EOS (ADO - ссылки для настольных баз данных Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32b76259f9be90ebd60cbc8c618a4d2bb80de165
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870123"
---
# <a name="eos-property-ado"></a><span data-ttu-id="7f3b5-102">Свойство EOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f3b5-102">EOS property (ADO)</span></span>


<span data-ttu-id="7f3b5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f3b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f3b5-104">Указывает, является ли текущую позицию в конце потока.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="7f3b5-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7f3b5-105">Return values</span></span>

<span data-ttu-id="7f3b5-106">Возвращает **логическое** значение, указывающее, является ли текущую позицию в конце потока.</span><span class="sxs-lookup"><span data-stu-id="7f3b5-106">Returns a **Boolean** value that indicates whether the current position is at the end of the stream.</span></span> <span data-ttu-id="7f3b5-107">**EOS** возвращает **значение True,** Если нет больше байтов в поток; Если существует несколько байт после текущего положения возвращает **значение False** .</span><span class="sxs-lookup"><span data-stu-id="7f3b5-107">**EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="7f3b5-108">Чтобы задать конец потока позицию, используйте метод [SetEOS](seteos-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7f3b5-108">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method.</span></span> <span data-ttu-id="7f3b5-109">Чтобы определить текущую позицию, используйте свойство [положение](position-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7f3b5-109">To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

