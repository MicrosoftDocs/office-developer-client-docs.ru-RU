---
title: ChangePassword Method (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bd2f5d87c6f90e940858ce5c6e01099c5e539d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480107"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="cedd0-102">ChangePassword Method (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cedd0-102">ChangePassword Method (ADOX)</span></span>


<span data-ttu-id="cedd0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cedd0-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="cedd0-104">Изменение пароля для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="cedd0-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="cedd0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cedd0-105">Syntax</span></span>

<span data-ttu-id="cedd0-106">*Пользователь*. Изменение пароля*Старый_пароль*, *Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="cedd0-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="cedd0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cedd0-107">Parameters</span></span>

  - <span data-ttu-id="cedd0-108">*Старый_пароль*</span><span class="sxs-lookup"><span data-stu-id="cedd0-108">*OldPassword*</span></span>

  - <span data-ttu-id="cedd0-109">**Строковое** значение, задающее существующий пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="cedd0-109">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="cedd0-110">Если у пользователя нет в настоящее время пароль, укажите пустую строку ("») для *Старый_пароль*.</span><span class="sxs-lookup"><span data-stu-id="cedd0-110">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

  - <span data-ttu-id="cedd0-111">*Новый_пароль*</span><span class="sxs-lookup"><span data-stu-id="cedd0-111">*NewPassword*</span></span>

  - <span data-ttu-id="cedd0-112">**Строковое** значение, задающее новый пароль.</span><span class="sxs-lookup"><span data-stu-id="cedd0-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="cedd0-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="cedd0-113">Remarks</span></span>

<span data-ttu-id="cedd0-114">По соображениям безопасности старый пароль должен быть указан в дополнение к новый пароль.</span><span class="sxs-lookup"><span data-stu-id="cedd0-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="cedd0-115">Если поставщик поддерживает администрирования свойства доверенного лица, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="cedd0-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

