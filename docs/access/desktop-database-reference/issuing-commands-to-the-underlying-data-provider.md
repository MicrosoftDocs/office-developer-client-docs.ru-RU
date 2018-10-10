---
title: Issuing Commands to the Underlying Data Provider
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480850"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="34d25-102">Issuing Commands to the Underlying Data Provider</span><span class="sxs-lookup"><span data-stu-id="34d25-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="34d25-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34d25-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34d25-104">Любые команды, не начинается с ФИГУРЫ передается через поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="34d25-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="34d25-105">Это эквивалентно команды фигуры в форме «ФИГУРЫ {поставщика команды}».</span><span class="sxs-lookup"><span data-stu-id="34d25-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="34d25-106">Выполните эти команды *не* имеет для создания **записей**.</span><span class="sxs-lookup"><span data-stu-id="34d25-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="34d25-107">Для экземпляра «ФИГУРЫ {РАЗМЕЩЕНИЯ ТАБЛИЦУ MyTable} — это команда действителен фигуры, при условии, что поставщик данных поддерживает размещения сообщений в ТАБЛИЦЕ.</span><span class="sxs-lookup"><span data-stu-id="34d25-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="34d25-108">Эта возможность позволяет как обычный поставщика команды и фигуры для совместного использования одного подключения и транзакций.</span><span class="sxs-lookup"><span data-stu-id="34d25-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

