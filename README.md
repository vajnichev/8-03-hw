# Домашнее задание к занятию "GitLab" - `Важничев Георгий`


### Задание 1

`**Что нужно сделать:**`

1. `Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.`
2. `Создайте новый проект и пустой репозиторий в нём.`
3. `Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.`

`В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.`


1. `Gitlab установлен `

![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.1.png)

2. `Создайте новый проект и пустой репозиторий в нём.`

![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.2.png)

3. `Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.`

![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.3.png)
![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.4.png)



### Задание 2

`Что нужно сделать:`

1. `Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.`
2. `Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.`

`В качестве ответа в шаблон с решением добавьте:`

`файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне`
`скриншоты с успешно собранными сборками.`

1. `Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.`

![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.7.png)

2. `Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.`
```yaml
stages:
  - test
  - build

test_go_1:
  stage: test
  image: golang:1.17
  script:
   - go test .
  tags:
   - ���netology

build_job_1:
  stage: build
  image: docker:latest
  script:
   - docker build .
  tags:
   - ���netology
```
![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.5.png)
![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.6.png)
![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.8.png)
![img](https://github.com/vajnichev/8-03-hw/blob/master/img/8.4.9.png)
