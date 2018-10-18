---
title: Specifying Threads Per Processor on IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5041eb32397fc9a234d0e4a0fff622f31b56a0a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603359"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="51228-102">Specifying Threads Per Processor on IIS</span><span class="sxs-lookup"><span data-stu-id="51228-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="51228-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="51228-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="51228-104"><<<<<<< HEAD при использовании служб удаленных рабочих СТОЛОВ с помощью Internet Information Services 4.0 или более поздней версии, количество потоков, созданных на процессор можно управлять с помощью управления реестра на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="51228-104"><<<<<<< HEAD When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server.</span></span> <span data-ttu-id="51228-105">Количество потоков процессора может повлиять на производительность в случае большой сетевой трафик, или в ситуациях низкой трафика с помощью запроса большого размера.</span><span class="sxs-lookup"><span data-stu-id="51228-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="51228-106">Пользователю следует проверить для достижения наилучших результатов.</span><span class="sxs-lookup"><span data-stu-id="51228-106">The user should experiment for best results.</span></span>
<span data-ttu-id="51228-107">=== При использовании служб удаленных рабочих СТОЛОВ с помощью Internet Information Services 4.0 или более поздней версии, количество потоков, созданных на процессор можно управлять с помощью управления реестра на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="51228-107">======= When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="51228-108">Количество потоков процессора может повлиять на производительность в случае большой сетевой трафик, или в ситуациях низкой трафика с помощью запроса большого размера.</span><span class="sxs-lookup"><span data-stu-id="51228-108">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="51228-109">Пользователю следует проверить для достижения наилучших результатов.</span><span class="sxs-lookup"><span data-stu-id="51228-109">The user should experiment for best results.</span></span>
>>>>>>> <span data-ttu-id="51228-110">master</span><span class="sxs-lookup"><span data-stu-id="51228-110">master</span></span>

<span data-ttu-id="51228-111">Метод, используемый для определения и измените значение по умолчанию для этого параметра зависит от конфигурации сервера IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="51228-111">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="51228-112">С MDAC 2.1.2.4202.3 (Джорджия) или более поздней версии на сервере IIS использует служб удаленных рабочих СТОЛОВ же службы компонентов (или транзакций Microsoft Services, если вы используете Windows NT) пул потоков как ASP сценариев использования.</span><span class="sxs-lookup"><span data-stu-id="51228-112">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use.</span></span> <span data-ttu-id="51228-113">Значение по умолчанию для числа потоков на процессор — 10.</span><span class="sxs-lookup"><span data-stu-id="51228-113">The default value for the number of threads per processor is 10.</span></span> <span data-ttu-id="51228-114">Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел реестра сервера:</span><span class="sxs-lookup"><span data-stu-id="51228-114">To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="51228-115">где *MaxPoolThreads* — REG\_значение DWORD.</span><span class="sxs-lookup"><span data-stu-id="51228-115">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="51228-116">*MaxPoolThreads* не отображается в реестре, если он добавляется в частности.</span><span class="sxs-lookup"><span data-stu-id="51228-116">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="51228-117">Диапазон допустимых значений от 5 рекомендуемый максимум 20.</span><span class="sxs-lookup"><span data-stu-id="51228-117">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="51228-118">Если значение, указанное в ключе реестра больше, чем значение параметра *PoolThreadLimit* (находится в разделе тот же путь), используется значение *PoolThreadLimit* .</span><span class="sxs-lookup"><span data-stu-id="51228-118">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="51228-119">Кроме того Если MDAC 2.1 2.1.1.3711.11 (Джорджия) или более ранних версий установлен на сервере служб IIS, значение по умолчанию для числа потоков процессора, 6.</span><span class="sxs-lookup"><span data-stu-id="51228-119">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6.</span></span> <span data-ttu-id="51228-120">Чтобы изменить значение по умолчанию, необходимо добавить следующий раздел реестра на сервере IIS:</span><span class="sxs-lookup"><span data-stu-id="51228-120">To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="51228-121">где *ADCThreads* — REG\_значение DWORD.</span><span class="sxs-lookup"><span data-stu-id="51228-121">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="51228-122">*ADCThreads* не отображается в реестре, если он добавляется в частности.</span><span class="sxs-lookup"><span data-stu-id="51228-122">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="51228-123">Диапазон допустимые значения — от 1 до 50.</span><span class="sxs-lookup"><span data-stu-id="51228-123">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="51228-124">Если значение, указанное в ключе реестра больше 50, максимальное значение — используемых (50).</span><span class="sxs-lookup"><span data-stu-id="51228-124">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

