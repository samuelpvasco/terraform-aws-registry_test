# terraform-aws-registry-test

Este repositório é um módulo Terraform minimalista projetado especificamente para **testes de integração, publicação e versionamento no Terraform Registry**.

O objetivo não é fornecer uma solução de infraestrutura complexa, mas sim servir como um "Hello World" para validar fluxos de CI/CD, visualização de documentação e comportamento do provedor AWS dentro do ecossistema do Registry.

---

## 🎯 Objetivo dos Testes
- Validar a publicação automática via **GitHub Releases**.
- Verificar a renderização de **Inputs** e **Outputs** na interface do Registry.
- Testar a compatibilidade de versões e restrições de provedores.

---

## 💻 Exemplo de Uso

Para testar a chamada deste módulo, você pode utilizar o bloco abaixo:

```hcl
module "registry_check" {
  source  = "<SEU_USUARIO>/registry-test/aws"
  version = "0.0.1"

  test_string = "Validando o Registry"
}
