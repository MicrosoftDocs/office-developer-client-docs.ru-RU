---
title: Отправка команд базовому поставщику данных
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709616"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="3800b-102">Отправка команд базовому поставщику данных</span><span class="sxs-lookup"><span data-stu-id="3800b-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="3800b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3800b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3800b-104">Любые команды, не начинается с ФИГУРЫ передается через поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="3800b-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="3800b-105">Это эквивалентно команды фигуры в форме «ФИГУРЫ {поставщика команды}».</span><span class="sxs-lookup"><span data-stu-id="3800b-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="3800b-106">Выполните эти команды *не* имеет для создания **записей**.</span><span class="sxs-lookup"><span data-stu-id="3800b-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="3800b-107">Для экземпляра «ФИГУРЫ {РАЗМЕЩЕНИЯ ТАБЛИЦУ MyTable} — это команда действителен фигуры, при условии, что поставщик данных поддерживает размещения сообщений в ТАБЛИЦЕ.</span><span class="sxs-lookup"><span data-stu-id="3800b-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="3800b-108">Эта возможность позволяет как обычный поставщика команды и фигуры для совместного использования одного подключения и транзакций.</span><span class="sxs-lookup"><span data-stu-id="3800b-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

