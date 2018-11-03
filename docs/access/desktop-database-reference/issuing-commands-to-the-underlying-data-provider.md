---
title: Выполнения команд базового поставщика данных
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 142772aaff5080a6e2522ab31884f2ff2319c8a7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944636"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="b75e6-102">Выполнения команд базового поставщика данных</span><span class="sxs-lookup"><span data-stu-id="b75e6-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="b75e6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b75e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b75e6-104">Любые команды, не начинается с ФИГУРЫ передается через поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="b75e6-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="b75e6-105">Это эквивалентно команды фигуры в форме «ФИГУРЫ {поставщика команды}».</span><span class="sxs-lookup"><span data-stu-id="b75e6-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="b75e6-106">Выполните эти команды *не* имеет для создания **записей**.</span><span class="sxs-lookup"><span data-stu-id="b75e6-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="b75e6-107">Для экземпляра «ФИГУРЫ {РАЗМЕЩЕНИЯ ТАБЛИЦУ MyTable} — это команда действителен фигуры, при условии, что поставщик данных поддерживает размещения сообщений в ТАБЛИЦЕ.</span><span class="sxs-lookup"><span data-stu-id="b75e6-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="b75e6-108">Эта возможность позволяет как обычный поставщика команды и фигуры для совместного использования одного подключения и транзакций.</span><span class="sxs-lookup"><span data-stu-id="b75e6-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

