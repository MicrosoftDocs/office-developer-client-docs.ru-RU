---
title: Свойство EOS (ADO - ссылки для настольных баз данных Access))
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481382"
---
# <a name="eos-property-ado"></a><span data-ttu-id="34743-102">EOS Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="34743-102">EOS Property (ADO)</span></span>


<span data-ttu-id="34743-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34743-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34743-104">Указывает, является ли текущую позицию в конце потока.</span><span class="sxs-lookup"><span data-stu-id="34743-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="34743-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="34743-105">Return Values</span></span>

<span data-ttu-id="34743-106">Возвращает **логическое** значение, указывающее, является ли текущую позицию в конце потока.</span><span class="sxs-lookup"><span data-stu-id="34743-106">Returns a **Boolean** value that indicates whether the current position is at the end of the stream.</span></span> <span data-ttu-id="34743-107">**EOS** возвращает **значение True,** Если нет больше байтов в поток; Если существует несколько байт после текущего положения возвращает **значение False** .</span><span class="sxs-lookup"><span data-stu-id="34743-107">**EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="34743-108">Чтобы задать конец потока позицию, используйте метод [SetEOS](seteos-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="34743-108">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method.</span></span> <span data-ttu-id="34743-109">Чтобы определить текущую позицию, используйте свойство [положение](position-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="34743-109">To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

