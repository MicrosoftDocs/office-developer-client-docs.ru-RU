---
title: TRANSACTION Statement (Microsoft Access SQL)
TOCTitle: TRANSACTION Statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 13628ee6d384430691475eb06dbbbdce4e980103
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481561"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="e4b06-102">TRANSACTION Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e4b06-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="e4b06-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4b06-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e4b06-104">Используется для начинать и завершать явные операции.</span><span class="sxs-lookup"><span data-stu-id="e4b06-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b06-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b06-105">Syntax</span></span>

<span data-ttu-id="e4b06-106">Начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="e4b06-106">Initiate a new transaction.</span></span>

<span data-ttu-id="e4b06-107">НАЧАТЬ ТРАНЗАКЦИЮ</span><span class="sxs-lookup"><span data-stu-id="e4b06-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="e4b06-108">Завершение операции с возвращением действия выполняются во время операции.</span><span class="sxs-lookup"><span data-stu-id="e4b06-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="e4b06-109">ФИКСАЦИЯ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="e4b06-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="e4b06-110">Завершение операции с откат всех выполненной во время операции.</span><span class="sxs-lookup"><span data-stu-id="e4b06-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="e4b06-111">ОТКАТ \[ТРАНЗАКЦИЙ | РАБОТА\]</span><span class="sxs-lookup"><span data-stu-id="e4b06-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b06-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="e4b06-112">Remarks</span></span>

<span data-ttu-id="e4b06-113">Не удалось автоматически запустить транзакции.</span><span class="sxs-lookup"><span data-stu-id="e4b06-113">Transactions are not started automatically.</span></span> <span data-ttu-id="e4b06-114">Чтобы запустить операцию, необходимо выполнить явно использовать команду НАЧАТЬ ТРАНЗАКЦИЙ.</span><span class="sxs-lookup"><span data-stu-id="e4b06-114">To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="e4b06-115">Операции могут быть вложенными до пяти уровней вложенности.</span><span class="sxs-lookup"><span data-stu-id="e4b06-115">Transactions can be nested up to five levels deep.</span></span> <span data-ttu-id="e4b06-116">Чтобы начать вложенных транзакций, используйте приступить к ТРАНЗАКЦИЙ в контексте существующей транзакции.</span><span class="sxs-lookup"><span data-stu-id="e4b06-116">To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="e4b06-117">Транзакции не поддерживаются для связанных таблиц.</span><span class="sxs-lookup"><span data-stu-id="e4b06-117">Transactions are not supported for linked tables.</span></span>

