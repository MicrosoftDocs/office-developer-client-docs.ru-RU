---
title: Инструкция TRANSACTION (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314149"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="f8fb2-102">Инструкция TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f8fb2-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="f8fb2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8fb2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8fb2-104">Позволяет начинать и завершать явные транзакции.</span><span class="sxs-lookup"><span data-stu-id="f8fb2-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8fb2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8fb2-105">Syntax</span></span>

<span data-ttu-id="f8fb2-106">**Начало новой транзакции**:</span><span class="sxs-lookup"><span data-stu-id="f8fb2-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="f8fb2-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="f8fb2-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="f8fb2-108">**Завершение транзакции с возвращением результата, полученного во время нее**:</span><span class="sxs-lookup"><span data-stu-id="f8fb2-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="f8fb2-109">COMMIT \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="f8fb2-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="f8fb2-110">**Завершение транзакции с отменой всех действий, выполненных во время нее**:</span><span class="sxs-lookup"><span data-stu-id="f8fb2-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="f8fb2-111">ROLLBACK \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="f8fb2-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="f8fb2-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8fb2-112">Remarks</span></span>

<span data-ttu-id="f8fb2-113">Транзакции не запускаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8fb2-113">Transactions are not started automatically.</span></span> <span data-ttu-id="f8fb2-114">Чтобы запустить транзакцию, необходимо явно использовать команду BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="f8fb2-114">To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="f8fb2-115">У транзакций может быть до пяти уровней вложенности.</span><span class="sxs-lookup"><span data-stu-id="f8fb2-115">Transactions can be nested up to five levels deep.</span></span> <span data-ttu-id="f8fb2-116">Чтобы запустить вложенную транзакцию, используйте команду BEGIN TRANSACTION внутри существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="f8fb2-116">To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="f8fb2-117">Транзакции не поддерживаются в связанных таблицах.</span><span class="sxs-lookup"><span data-stu-id="f8fb2-117">Transactions are not supported for linked tables.</span></span>

