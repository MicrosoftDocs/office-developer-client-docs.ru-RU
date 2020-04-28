---
title: Указание числа потоков на процессор в IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308591"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="9ecec-102">Указание числа потоков на процессор в IIS</span><span class="sxs-lookup"><span data-stu-id="9ecec-102">Specifying threads per processor on IIS</span></span>


<span data-ttu-id="9ecec-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ecec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ecec-104">При использовании RDS в службах IIS 4,0 или более поздней версии число потоков, созданных на процессор, можно контролировать, управляя реестром на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="9ecec-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="9ecec-105">Количество потоков на процессор может повлиять на производительность при высоком трафике или в случае недостаточного объема запросов с большим размером.</span><span class="sxs-lookup"><span data-stu-id="9ecec-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="9ecec-106">Для достижения лучших результатов пользователь должен экспериментировать.</span><span class="sxs-lookup"><span data-stu-id="9ecec-106">The user should experiment for best results.</span></span>

<span data-ttu-id="9ecec-107">Метод, используемый для определения и изменения значения по умолчанию для этого параметра, зависит от конфигурации сервера IIS 4,0.</span><span class="sxs-lookup"><span data-stu-id="9ecec-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="9ecec-108">С помощью MDAC 2.1.2.4202.3 (GA) или более поздней версии, установленной на сервере IIS, RDS использует те же службы компонентов (или Microsoft Transaction Services, если вы используете Windows NT) для пула потоков, используемого скриптами ASP.</span><span class="sxs-lookup"><span data-stu-id="9ecec-108">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use.</span></span> <span data-ttu-id="9ecec-109">Значение по умолчанию для количества потоков на процессор — 10.</span><span class="sxs-lookup"><span data-stu-id="9ecec-109">The default value for the number of threads per processor is 10.</span></span> <span data-ttu-id="9ecec-110">Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел в реестр сервера:</span><span class="sxs-lookup"><span data-stu-id="9ecec-110">To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="9ecec-111">где *макспулсреадс* — это параметр\_reg.</span><span class="sxs-lookup"><span data-stu-id="9ecec-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="9ecec-112">*Макспулсреадс* не отображается в реестре, если он специально не добавлен.</span><span class="sxs-lookup"><span data-stu-id="9ecec-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="9ecec-113">Диапазон допустимых значений: от 5 до рекомендуемого максимума 20.</span><span class="sxs-lookup"><span data-stu-id="9ecec-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="9ecec-114">Если значение, заданное в разделе реестра, больше значения ключа *пулсреадлимит* (расположенного по тому же пути), используется значение *пулсреадлимит* .</span><span class="sxs-lookup"><span data-stu-id="9ecec-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="9ecec-115">Кроме того, если на сервере IIS установлен MDAC 2,1 2.1.1.3711.11 (GA) или более ранней версии, значение по умолчанию для количества потоков на процессор составляет 6.</span><span class="sxs-lookup"><span data-stu-id="9ecec-115">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6.</span></span> <span data-ttu-id="9ecec-116">Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел в реестр на сервере IIS:</span><span class="sxs-lookup"><span data-stu-id="9ecec-116">To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="9ecec-117">где *адксреадс* — это параметр\_reg.</span><span class="sxs-lookup"><span data-stu-id="9ecec-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="9ecec-118">*Адксреадс* не отображается в реестре, если он специально не добавлен.</span><span class="sxs-lookup"><span data-stu-id="9ecec-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="9ecec-119">Допустимые значения: от 1 до 50.</span><span class="sxs-lookup"><span data-stu-id="9ecec-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="9ecec-120">Если значение, указанное в разделе реестра, превышает 50, то используется максимальное значение (50).</span><span class="sxs-lookup"><span data-stu-id="9ecec-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

