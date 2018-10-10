---
title: DBEngine.DefaultPassword Property (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5b1195b4217ca72374402b361b09d540583bf06
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483096"
---
# <a name="dbenginedefaultpassword-property-dao"></a><span data-ttu-id="01cbe-102">DBEngine.DefaultPassword Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="01cbe-102">DBEngine.DefaultPassword Property (DAO)</span></span>


<span data-ttu-id="01cbe-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="01cbe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="01cbe-104">Задает пароль, используемый для создания **рабочей области** по умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="01cbe-104">Sets the password used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="01cbe-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="01cbe-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="01cbe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01cbe-106">Syntax</span></span>

<span data-ttu-id="01cbe-107">*выражение* . DefaultPassword</span><span class="sxs-lookup"><span data-stu-id="01cbe-107">*expression* .DefaultPassword</span></span>

<span data-ttu-id="01cbe-108">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="01cbe-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="01cbe-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="01cbe-109">Remarks</span></span>

<span data-ttu-id="01cbe-110">Параметр **DefaultPassword** — это тип данных String, который может иметь длину до 20 знаков.</span><span class="sxs-lookup"><span data-stu-id="01cbe-110">The setting for **DefaultPassword** is a String data type that can be up to 20 characters long.</span></span> <span data-ttu-id="01cbe-111">Он может содержать любой символ, за исключением ASCII 0.</span><span class="sxs-lookup"><span data-stu-id="01cbe-111">It can contain any character except ASCII 0.</span></span>


> [!NOTE]
> <P><span data-ttu-id="01cbe-112">Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="01cbe-112">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="01cbe-113">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="01cbe-113">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="01cbe-114">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="01cbe-114">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="01cbe-115">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="01cbe-115">Weak password: House27.</span></span> <span data-ttu-id="01cbe-116">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="01cbe-116">Use a strong password that you can remember so that you don't have to write it down.</span></span></P>



<span data-ttu-id="01cbe-117">По умолчанию, свойство **DefaultUser** имеет значение «администратор» и **DefaultPassword** свойству в строку нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="01cbe-117">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="01cbe-118">Как правило метод **CreateWorkspace** используется для создания объекта **рабочей области** через заданное имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="01cbe-118">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password.</span></span> <span data-ttu-id="01cbe-119">Тем не менее для обеспечения обратной совместимости с предыдущими версиями и для удобства при реализации защищенной базы данных не ядро базы данных Microsoft Access автоматически создает объект **рабочей области** по умолчанию, когда требуется, если он не является open.</span><span class="sxs-lookup"><span data-stu-id="01cbe-119">However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open.</span></span> <span data-ttu-id="01cbe-120">В этом случае значения свойств **DefaultUser** и **DefaultPassword** определить имя пользователя и пароль для объекта **рабочей области** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01cbe-120">In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="01cbe-121">Для этого свойства вступили в силу следует устанавливать до вызова метода любые методы DAO.</span><span class="sxs-lookup"><span data-stu-id="01cbe-121">For this property to take effect, you should set it before calling any DAO methods.</span></span>

