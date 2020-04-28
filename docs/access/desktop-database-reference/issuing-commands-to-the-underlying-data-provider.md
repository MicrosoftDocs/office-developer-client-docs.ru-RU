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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291090"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="67769-102">Отправка команд базовому поставщику данных</span><span class="sxs-lookup"><span data-stu-id="67769-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="67769-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67769-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67769-104">Любая команда, не начинающаяся с фигуры, передается поставщику данных.</span><span class="sxs-lookup"><span data-stu-id="67769-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="67769-105">Это эквивалентно выдаче команды фигуры в форме "SHAPE {Provider Command}".</span><span class="sxs-lookup"><span data-stu-id="67769-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="67769-106">Этим командам *не* требуется создавать **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="67769-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="67769-107">Например, "SHAPE {DROP TABLE MyTable}" — это вполне действительная команда Shape, предполагая, что поставщик данных поддерживает DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="67769-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="67769-108">Эта возможность позволяет обычным поставщикам команд и командам форм совместно использовать одно и то же подключение и транзакцию.</span><span class="sxs-lookup"><span data-stu-id="67769-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

